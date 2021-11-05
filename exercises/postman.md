# Postman

This exercise aims to learn how to create a Postman collection for easy api testing and monitoring. On the way, you will learn how to read curl commands to fire http requests from the command line, if you did not know yet.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks. This is your submission for the exercise.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task and provide code snippets and screenshots if needed.
- If you are not able to solve the task because you are not getting the tool to work, describe how you would solve it theoretically. You should still provide e.g. code snippets or a step by step description from the documentation or tutorial you found.
- Provide a hyperlink or other reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- Submit at __least two, but not more than four A4 pages__ for your exercise documentation in pdf format.

## Tasks

1. Download the Postman client or [use Postman in your browser](https://web.postman.co/). I recommend using the client. We will fire a few requests against some endpoints of an api, test, and monitor them.
2. Create a collection for the requests with a descriptive name. You can also define variables, put in the variable 'baseUrl' with the value 'https://httpbin-wm2jlcjqfa-ey.a.run.app'.
3. Add a new request to this collection as an equivalent to the following curl command. A successful request is indicated through a '200 OK' status.

    ```bash
    curl -X GET "{{baseUrl}}/image" -H "accept: image/jpeg"
    ```

    - Describe in words how you created the request in Postman.
    - What is the response that you get?

4. Add a new request for this curl command, which uses a bearer token:

    ```bash
    curl -X GET "{{baseUrl}}/bearer" -H "accept: application/json" -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkphbmUgQmVhciIsImdyb3VwIjoiZGV2ZWxvcGVyIiwiaWF0IjoxNTE2MjM5MDIyfQ.9WSqLT7Lva8UeaQDdDMlwIABJTUI-vFJ3Sa1FqqpFpA"
    ```

    - Describe in words how you created the request in Postman.
    - What is the response that you get?
    - What is the purpose of such a request?
    - Save the bearer token as a variable named 'token' instead of using it in plaintext. What changes did you make in the request?
    - What is the payload of the bearer token?
    - Is there any other information you can get from the token?

5. Add the following tests to the request of task 4:

    ```js
    pm.test("Status code is 200", () => {
        pm.expect(pm.response.code).to.eql(200);
    });

    pm.test("The response has all properties", () => {
        const responseJson = pm.response.json();
        pm.expect(responseJson.authenticated).to.eql(true);
        pm.expect(responseJson.token).to.be.a('string');
        pm.expect(responseJson.token).to.eql(pm.variables.get("token"));
    });
    ```

    - Describe in words how you integrated the tests for the request in Postman.
    - Describe in words what the tests are actually testing in detail.
    - Run the tests successfully when you send the request again?

6. Create a monitor for the collection. Set an hourly frequency to run the monitor. If you don't want to wait for the scheduled execution, run the monitor manually a few times. Describe what the monitor does and how this would help you as a developer.

7. Can you think of use cases for Postman? When could this tool help you?

## This will help you

- Using a search engine
- [Using Postman Online](https://web.postman.co/)
- [Learning about Postman](https://learning.postman.com/)
- [JWT Token Encoder/Decoder](https://jwt.io/)
