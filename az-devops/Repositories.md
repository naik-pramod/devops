### Supported Repos
YAML pipelines only work with certain version control systems.
 - Azure Repos Git
 - GitHub
 - GitHub Enterprise Server
 - Bitbucket Cloud

### CI triggers
CI triggers cause a pipeline to run whenever you push an update to the specified branches or you push specified tags.

We can specify pipeline triggers in 3 ways:
### 1.  CI 
  - Two types of Filters:
    - Branch Filters
    - Path Filters

#### A pipeline with no CI trigger
trigger: none

```
  trigger:
   - master
   - releases/*
   ```
#### YAML pipelines can be triggered when tags are added to a commit.

- Tags
- PR
   To enable pull request validation in Azure Git Repos, navigate to the branch policies for the desired branch, and configure the Build validation policy for that branch

### 2. Scheduled
### 3. Build Completion

### Classic Pipeline Configuration

![azpipeline](/az-devops/images/classic-pipeline.PNG)


|Tasks| **Description** |
|-----|-------------|
|**Pipeline**| |
|`...`Used to add Agent Job/Agentless Job to the pipeline| *Name:* <br /> Specify pipeline's name|
|| *Agent Pool:* <br /> Select Agent Pool.  Instead of managing each agent individually, <br /> you organize agents into agent pools.|
|| *Agent Specification:* <br /> Select Agent Spec. such as   windows-latest, macos-latest, ubuntu-18.4 etc..|
|**Get Sources**||
|| *Select Sources*<br />Select a Source, such as Azure Git Repo, Github.. |
||*Team Project*<br /> Select Project|
||*Repository*<br /> Select Repo from Project|
||*Default branch for manual and scheduled builds*<br /> Select Branch |
||*Clean*<br /> Select `true` or `False` to clean working directory before running the build |
||*Clean Options*<br /> Select `Sources`/`Source and Output directory`/`Sources directory`/`All build Directory`|
||*Tag Sources*<br /> Select `Never`/`Always`/`on Success`. On every build or every successful build, tag your source code files to identify which version of each file is included in the completed build.|
||*Tag Format*<br /> Feed format, could be a combination of user-defined or pre-defined variables that have a scope of "All". For example: '$(Build.DefinitionName)_$(Build.DefinitionVersion)_$(Build.BuildId)_$(Build.BuildNumber)_$(My.Variable)'|
||*Report Build Status*<br />Displays a badge on the source repository to indicate whether the build succeeded or failed.|
||*Checkout Submodules*<br />The build pipeline will check out your Git submodules if they are in the same repository or in a public repository|
||*Don't sync Sources*<br />|
||*Shallow fetch*<br />When selected, limit fetching to the specified number of commits from the tip of each remote branch history. You can specify the number of commits to fetch in Fetch depth option|
|**Agent JOB**||
|A job is a logical grouping of tasks that defines the runtime target on which the tasks will execute. An agent job executes tasks on an agent in an agent pool.||
||*Display Name*<br />Set the Job's display Name |
||*Agent Pool*<br /> Select agent Pool. When you queue a build, it executes on an agent from the selected pool. You can select a Microsoft-hosted pool, or a self-hosted pool that you manage.|





