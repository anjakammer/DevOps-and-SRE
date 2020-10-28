# git and GitHub

The aim of this exercise is to learn how to use git together with GitHub. Furthermore, this exercise should encourage you to look for instructions of tools on the internet.
Basically, git is a tool to work with code and its versions, bundled in a repository.
GitHub is a platform for storing and accessing these repositories remotely. There are also additional features such as forks and pull requests.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks. This is your submission for the exercise.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task and provide code snippets and screenshots if needed.
- If you are not able to solve the task because you are not getting the tool to work, describe how you would solve it theoretically. You should still provide e.g. code snippets or a step by step description from the documentation or tutorial you found.
- Provide a hyperlink or other reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- Try to submit not more than two A4 pages for your exercise documentation in pdf format.

## Tasks

1. Create a [GitHub](https://github.com/) account or use your present one.
2. Fork the following repository and clone it to your local machine: [https://github.com/anjakammer/git-and-github-exercise](https://github.com/anjakammer/git-and-github-exercise)
3. Install and use the git command line tool for all git related tasks, no client with an GUI, we want to work with the shell!
4. Create a new branch from the main branch. The name should be a UUID version 4 string.
5. Add this UUID to the list in the Readme file of the repository. Tag your commit also with the UUID like this: `v.<UUID>`
6. Push your change and the tag into your forked repository on GitHub. What changes can you observe in the GitHub repository?
7. Create a pull request with your change to merge it back into the base repository.

## This will help you

- using a search engine
- [git related articles](../deep-dive/development.md#articles) I curated for you
- [UUID Generator](https://www.uuidgenerator.net/)
- [git CLI](https://git-scm.com/downloads)
