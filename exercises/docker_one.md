# Docker (Part I)

This exercise aims to learn how to install the docker container runtime and cli on your system of choice. This component is needed for future exercises, so try not to skip it.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task and provide code snippets and screenshots if needed.
- If you are not able to solve the task because you are not getting the tool to work, describe how you would solve it theoretically. You should still provide e.g. code snippets or a step by step description from the documentation or tutorial you found.
- Provide a hyperlink or other reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- This part of the final submission should be described in at __least one, but not more than two A4 pages__. Do not submit this exercise alone, but together with the second part. If you did not do the second part, then you should submit what you have, of course.

## Tasks

1. Use this resource to install docker on your system: [https://docs.docker.com/get-docker](https://docs.docker.com/get-docker). What Problems occur?
2. Read the documentation for your platform carefully and describe shortly how docker is run technically. Does your system require to leverage a VM to run docker containers, or does it use your system kernel?
3. We want to run a linux container, do you need to make changes on your docker configuration, and why?
4. Reuse the code of the 'GitHub Actions Exercise'. If you missed that part, simply download the repository here: [https://github.com/anjakammer/github-actions-exercise](https://github.com/anjakammer/github-actions-exercise). Use the instructions in the README of the repository to run the container. Is there any documentation missing?
5. Access the web application in your browser: [http://localhost:8080](http://localhost:8080). What does it return exactly? If the application is not running on that address, try to debug this error.

## This will help you

- Using a search engine
- [Operation Tools: docker](./../deep-dive/operation.md#docker)
- If you are using Windows and you have problems with docker
  - ask the instructor!
  - if you absolutely cannot get the docker runtime set up properly, use a Linux VM with e.g. VirtualBox and a Linux VM Image with GUI. Here is tutorial on how to do that: [Install VirtualBox ->Ubuntu ->Docker on Windows 10](https://medium.com/@armstar/install-virtualbox-ubuntu-docker-on-windows-10-a16765a09b)
