### Azure Pipelines

Azure Pipelines automatically builds and tests code projects to make them available to others.

#### Define Pipelines
-  using YAML syntax
-  using the Classic interface

#### Concepts
![azpipeline](/az-devops/images/azpipeline.PNG)

#### Agent
An agent is computing infrastructure with installed agent software that runs one job at a time. 
For example, your job could run on a Microsoft-hosted Ubuntu agent

#### Approvals
Approvals define a set of validations required before a deployment runs. Manual approval is a common check performed to control deployments to production environments.

##### Artifact
An artifact is a collection of files or packages published by a run. Artifacts are made available to subsequent tasks, such as distribution or deployment.

#### Deployment
For YAML pipelines, a deployment typically refers to a deployment job. 
A deployment job is a collection of steps that are run sequentially against an environment. 
You can use strategies like run once, rolling, and canary for deployment jobs.

#### Environment
An environment is a collection of resources, where you deploy your application. 
It can contain one or more virtual machines, containers, web apps, or any service that's used to host the application being developed. 

A pipeline might deploy the app to one or more environments after build is completed and tests are run.

#### Manage pipeline variables
Use variables to store values or encrypted secrets separately from your repository.
To manage pipeline variables, edit your YAML pipeline and choose Variables.