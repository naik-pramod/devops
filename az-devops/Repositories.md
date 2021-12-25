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

|  Tasks | Variables   | Triggers    |Options |History|
|--------|-------------|-------------|--------|-------|
|- Pipeline |             |             |        |       |
|   - Name |  |  || |
|   - Agent Pool|||||||
|   - Agent Specification|||||
|   - Parameters|||||
- Select a Source 
   Azure Git Repo, Github..

- Team Project
   

- Repository
  

- Default branch for manual and scheduled builds

- Clean

- Clean Options

- 





