### Supported Repos
YAML pipelines only work with certain version control systems.
 - Azure Repos Git
 - GitHub
 - GitHub Enterprise Server
 - Bitbucket Cloud

### CI triggers
CI triggers cause a pipeline to run whenever you push an update to the specified branches or you push specified tags.

We can specify pipeline triggers in 3 ways:
1. CI 
  - Two types of Filters:
    - Branch Filters
    - Path Filters

```trigger:
   - master
   - releases/*`

2. Scheduled
3. Build Completion



