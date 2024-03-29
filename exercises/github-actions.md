# GitHub Actions

This exercise aims to learn how to automate any code-related process using GitHub Actions. You can see this tool as an example for many other similar automation tools.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks. This is your submission for the exercise.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task and provide code snippets and screenshots if needed.
- If you are not able to solve the task because you are not getting the tool to work, describe how you would solve it theoretically. You should still provide e.g. code snippets or a step by step description from the documentation or tutorial you found.
- Provide a plaintext URL or other reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- Submit at __least two, but not more than four A4 pages__ for your exercise documentation in pdf format.

## Tasks

1. Fork the repository [https://github.com/anjakammer/github-actions-exercise](https://github.com/anjakammer/github-actions-exercise) into your account and activate GitHub Actions under the tab "Actions". If there is no Actions tab, you probably need to [activate Actions for the Repository](https://github.com/anjakammer/DevOps-and-SRE/blob/master/exercises/github-actions.md#enabling-the-github-actions-feature).
2. Add a fancy image into the Readme.md file on a new branch and open a pull request on your own repository for your change. A GitHub Workflow should run now. How can you observe the workflow and its stages running for this pull request?
3. Why and when does the 'build' job run? When run the other two?
4. Analyse the GitHub Workflow configuration file `.github/workflows/onPullRequest.yml`. Explain in detail what each line of the configuration file means and does. These are about 50 lines, so you need to write down about __50 sentences__ for this task. However, some lines appear multiple times and some are blank.
5. How does your GitHub repository change after running this Workflow?
6. Can you think of any other use cases for GitHub Actions? What processes could you automate using this tool?

## This will help you

- Using a search engine

### Enabling the GitHub Actions Feature

Sometimes it is required for forked repositories to enable the GitHub Actions feature to use it.  
Create a (new) pull request after activating Actions, so the workflow is able to run.
> <img src="https://user-images.githubusercontent.com/7222193/141982113-ac561029-be82-41e1-962a-866810b88ef7.png" width="500">

### If this did not help or apply to your case, try this: 

See [the Documentation on that](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository)
> ![image](https://user-images.githubusercontent.com/7222193/141508716-a1699bb7-3f63-4712-a04b-4fe51628e914.png)

