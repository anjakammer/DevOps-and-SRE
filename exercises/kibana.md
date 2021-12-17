# Kibana

This exercise aims to learn how to use Kibana to search effectively for logs.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task and provide code snippets and screenshots if needed.
- If you are not able to solve the task because you are not getting the tool to work, describe how you would solve it theoretically. You should still provide e.g. code snippets or a step by step description from the documentation or tutorial you found.
- Provide a reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- Your submission should be described in __at least one, but not more than two A4 pages__.

## Tasks

1. Visit the [Demo Sections of elastic.co](https://www.elastic.co/de/demos), and launch a Kibana Demo session. Enter the menu <sub>![image](https://user-images.githubusercontent.com/7222193/146424569-c1af9657-fecc-4c16-b383-c4f90b620b38.png)</sub> and describe the following 3 Features.
Use the [Kibana Guide](https://www.elastic.co/guide/en/kibana/current/index.html) to explain their purpose, reference properly, please. 
  - Discover
  - Canvas
  - Maps
2. Go to 'Discover' and change the index pattern to "kibana_sample_data_flights". Describe what kind of data you see and a possible user-centered use case for that. Who is the user of this use case?
3. What is actually an index pattern in Kibana?
4. Filter for the following fields on the left: 'FlightNum', 'Origin', 'Dest', 'Cancelled', 'FlightDelay'. Describe how the view changes.
5. What fields are missing to actually be helpful for the use case you described in task 2, or another use case that comes to your mind that might fit the prior selected fields.
6. Select another index pattern of your choice, select the search field, and perform a useful query, using the Kibana Query Language (KQL) for a user and use case of your choice.

## This will help you

- Using a search engine
- [Kibana Guide](https://www.elastic.co/guide/en/kibana/current/index.html)
