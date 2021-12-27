### Classic Pipeline

#### New Classic Pipeline
Click on *New Pipeline*
![az-pipeline](/az-devops/images/new-pipeline.PNG)
#### Classic Pipeline Wizard
Select the Repository/Source
![az-pipeline](/az-devops/images/pipeline-type.png)
![az-pipeline](/az-devops/images/classic-newpipeline.png)
###### Supported Repos
YAML pipelines only work with certain version control systems.
 - Azure Repos Git
 - GitHub
 - GitHub Enterprise Server
 - Bitbucket Cloud
#### Configure Classic Pipeline
![az-pipeline](/az-devops/images/classic-pipeline.png)


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





