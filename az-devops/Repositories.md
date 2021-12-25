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

### Pipeline Configuration

|Tasks| **Description** |
|-----|-------------|
|**Pipeline**| |
|`...`Used to add Agent Job/Agentless Job to the pipeline| *Name:* <br /> Specify pipeline's name|
|| *Agent Pool:* <br /> Select Agent Pool.  Instead of managing each agent individually, <br /> you organize agents into agent pools.|
|| *Agent Specification:* <br /> Select Agent Spec. such as   windows-latest, macos-latest, ubuntu-18.4 etc..|
|||
|**Get Sources**||
|| *Select Sources*<br />Select a Source, such as Azure Git Repo, Github.. |
||*Team Project*<br /> Select Project|
||*Repository*<br /> Select Repo from Project|
||*Default branch for manual and scheduled builds*<br /> Select Branch |
||*Clean*<br /> Select `true` or `False` to clean working directory before running the build |
||*Clean Options*<br /> Select `Sources`/`Source and Output directory`/`Sources directory`/`All build Directory`|
||*Tag Sources*<br /> Select|


- 





