# Kubernetes

This exercise aims to learn how to use Kubernetes to deploy containerized applications.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task and provide code snippets and screenshots if needed.
- If you are not able to solve the task because you are not getting the tool to work, describe how you would solve it theoretically. You should still provide e.g. code snippets or a step by step description from the documentation or tutorial you found.
- Provide a reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- Your submission should be described in __at least one, but not more than three A4 pages__.

## Tasks

Visit the [interactive online course at katacoda](https://www.katacoda.com/courses/kubernetes/kubectl-run-containers). It uses minikube - a simpler version of Kubernetes. For every step, solve the tasks and answer the questions below. Don't forget to describe your progress during each tutorial step as described in the `Exercise Rules`.

- Step 1
  - What is actually 'kubectl', and for what is it used?
  - How many CPUs and how much memory will be provisioned for your minikube instance?
  - How many nodes are listed when you run `kubectl get nodes`?
- Step 2
  - How many replicas has the deployed application 'http'?
  - On what namespace is the application running?
  - You can spot the term 'ReplicaSet' in the deployment configuration; what is this, and why is it useful?
- Step 3
  - What does the command `kubectl expose`?
- Step 4
  - Why is it a bad idea to use `kubectl run` for production deployments?
  - 'svc' in `kubectl get svc` stands for service, what is a Kubernetes Service used for?
- Step 5
  - If there are not all 3 pods running when you execute `kubectl get pods`, give it a second and repeat the request.
  - What is the output for the last command `curl http://xxx.xx.x.xx:8000`?

## This will help you

- Using a search engine
- [The Illustrated Children’s Guide to Kubernetes - Phippy Goes to the Zoo](https://www.cncf.io/phippy-goes-to-the-zoo-book/)
