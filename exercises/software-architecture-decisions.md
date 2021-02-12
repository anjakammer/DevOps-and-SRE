# Software Architecture Decisions

This exercise aims to learn how to express and justify software architecture decisions.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks.
- Provide a reference for every source you used to solve a task. Paraphrase and cite correctly, please.
- Your submission should be described in __at least two, but not more than three A4 pages__.

## Tasks

You will create a document that describes and justifies certain software architecture decisions. You will be using all your knowledge that you acquired in this course. The software architecture you are working with is the web app 'The Shop' - a webshop for gaming pc hardware. You find the description here: [Scenario: The Shop](scenarios/the-shop.md).

1. Use the sentence fragments ([Skeleton](#skeleton)) and every term ([Terms to use](#terms-to-use)) at least once to build the architecture documentation. Provide always a comprehensive explanation for an architecture decision you made. Usually, such an explanation consists of several sentences, backed up by sources, best practices, or educated opinions (think of the lectures). Also, try to come up with pro and contra arguments. Don't panic - if you feel you cannot take a fact-based decision, just try to reasonably justify any decision that comes to your mind.
2. Provide a self-made diagram that shows an integral aspect of the architecture, when it comes to one of the following topics: CI/CD, compute platform and infrastructure, delegation of functionality to cloud-services, monitoring for SLIs, secrets management, scalability.

### Skeleton

#### Culture and Organization

- Every development team takes care of one to two application components (services), to keep the cognitive load at bay. All teams should work DevOps-driven, this means [ provide a comprehensive explanation ]
- A typical one-week sprint consists of the following Scrum-inspired meetings ... [ enumerate and provide a comprehensive explanation for each meeting ]
- A dedicated platform team of SREs supports the development teams with ... [ enumerate and provide a comprehensive explanation for each way to support a development team as an SRE ]

#### Management of SLOs

- The platform team is responsible for the development, measurement, and communication of SLOs. The methods and tools used for this are ... [ your description here. Also, think of meetings and collaboration in general ]

#### Application Development and Delivery

- There is a common way of developing and delivering new versions of components, which can be described as ... [ provide a comprehensive explanation ]
- Security is important to us because we are working with personal data. Secrets Management is a measure that we took recently to secure our customer's data and prevent malicious attacks on our infrastructure. The workflow to handle secrets ... [ provide a comprehensive explanation, it does not have to be the most secure and complex system but it has to be appropriate ]

#### Compute Platforms and Infrastructure

- There are several solutions for computing platforms, depending on the component needs ... [ provide a comprehensive explanation of which platform is used for what components. Provide at least two different solutions. ]
- The following software and infrastructure components are built in a modular way, so there is the possibility to exchange them with cloud-services if the demand and requirements can not be met cost-effectively by the internal development teams anymore ... [ enumerate and provide a comprehensive explanation for at least two components that could be exchanged by cloud services. You can also come up with components, that are not yet described. ]

#### Scaling for Black Friday

- There were special measures taken, to increase the scalability of the architecture at Black Friday, at moderate costs for the rest of the year. These measures consist of [ enumerate 5 measures and provide a comprehensive explanation for each of them ]

### Terms to use

Use other terms and concepts for your document too, that are not in this list.

- cross-functional
- autonomy
- communication
- knowledge sharing
- trust
- quality
- feedback
- reliability metric
- application artifact
- deployment manifest
- deployment workflow
- public cloud provider
- SLIs
- private cloud
- static content
- edge (computing)
- database
- pull-based deployment strategy

## This will help you

- Using a search engine
- your lecture summaries, exercise submissions, lecture slides
- [Deep Dive Section](../deep-dive/README.md)
