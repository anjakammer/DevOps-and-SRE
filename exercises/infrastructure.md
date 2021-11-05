# Infrastructure & Architecture

This exercise aims to learn how an application infrastructure and architecture for running web applications could look like and how it could be configured.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks. This is your submission for the exercise.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task and provide configuration snippets.
- If you are not able to solve the task, describe how you tried to find information, and what was confusing you.
- Provide a hyperlink or other reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- Submit at __least one, but not more than four A4 pages__ for your exercise documentation in pdf format.

## Tasks

1. Read the following architecture description with the help of the provided diagram to understand the communication flow of all showed components. Are there any questions or terms you do not know? Use a search engine and answer your questions yourself. Document the questions and solutions. Describe at least 3 terms from the text for this task.
2. For every component, provide a possible simplified configuration file that is needed for them to communicate with each other. It follows a list of key/value pairs - typically used as 'Environment Variables'. Each of them should appear at least once in one of the configuration files. That means every key/value pair in this list is needed for one or many component configurations. Add any other key/value pair to the configuration files that you think is missing in this list:
   - Auth_Credentials = '[{"name":"user1","group":"admin","pwd":"*obzHaWEQoWu8F2sZ7g9.XdGARJWRQ"},{"name":"user2","group":"admin","pwd":"bK7YhVdrLeNbbDvB2.XuX@cFZ4Ct@h"}]'
   - DB_Connection_String = 'jdbc:postgresql://cluster.web-service.db.example:5342/postgres?user=name&password=secret&ssl=true'
   - Cache_Connection_String = 'redis://clientid:password@cluster.web-service.cache.example:6380?ssl=true&db=1'
   - Api_Key = 'Kwm7@u4CHQF*W.9NpPTHfeZvEdPffs'
   - Service_A_Host_Name = 'cluster.web-service.a.example'
   - Service_B_Host_Name = 'cluster.web-service.b.example'
   - Service_A_Port = 8080
   - Service_B_Port = 8081
   - Proxy_Port = 80
   - Cache_Port = 6380
   - DB_Port = 5342
   - DB_User = 'name'
   - Cache_User = 'clientid'
   - DB_psw = 'secret'
   - Cache_psw = 'password'
3. What components are infrastructural components?

### Architecture Description

This is an architecture for a web-based HR management application, that means, the users of this system are employees of the HR department of some company. This web application is accessible over the public internet so that the HR employees can work from home.

#### Component 'Proxy'

The proxy ingests all internet traffic that comes in from port 80 to the application and uses basic auth for authentication and authorization of the users that log in. Everybody knows, that this is not a safe way to do authentication - but the priority for security is not that high in that organization. After successful authentication and authorization, the proxy directs the traffic to 'Service A'.

#### Component 'Service A'

Service A is the heart of the application - it does data aggregations and CRUD Operations on the resources (employees, salaries, bonuses, and contracts). Incoming requests from port 8080 are already authorized, so no further security checks are needed. For the CRUD operations, it uses a database and for maintaining user sessions - a cache. For salary and bonus calculations, Service A needs 'Service B'. Therefore, it makes API requests over HTTP to 'Service B' using an API key to authorize.

#### Component 'Service B'

Service B provides an API, secured by an API key. The API uses the HAL response format and provides a list of API endpoints for the requesting service, so the actual endpoints of Service B can change without changing the code of the requesting service. Every time a requesting service wants to do a calculation, it looks up the current endpoint structure to make the request - so there are at least 2 requests made by the requesting service to calculate a salary.
Example:

```json
{
   "health":"ok",
   "_links":{
      "self":{
         "href":"http://cluster.web-service.b.example:8081"
      },
      "calc-salary":{
         "href":"http://cluster.web-service.b.example:8081/salary?role={role}&department={department}",
         "templated":true
      },
      "calc-bonus":{
         "href":"http://cluster.web-service.b.example:8081/bonus?role={role}&department={department}&corporate_profit={profit-in-thousand}",
         "templated":true
      }
   }
}
```

To provide these HAL responses, Service B additionally needs to know its own DNS-Name to render the endpoint strings.

#### Component 'Cron'

The Cron component is scheduled to run every night at 3 am to do database operations. It looks for expiring employment contracts and alters a corresponding flag in the contract resource.

#### Component 'Database'

Is used to store and read out structured data.

#### Component 'Cache'

Is used to store user session data.

![Example Architecture](img/example-architecture.png)

## This will help you

- Using a search engine for terms you do not know

### Example Component Configuration file

```txt
# my-service.txt

   API_PWD : "superSecret",
   API_USER : "user1",
   PORT : 8888
```
