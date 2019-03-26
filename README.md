## Purpose

This is a collection of CloudFormation Templates.

## Source code structure

```bash
├── code_pipeline
│   └── pipeline.yaml                       <-- Cloudformation to create entire pipeline
├── buildspec.yml                           <-- CodeBuild spec                           
```
## CloudFormation will create the following resources:

* `code_pipeline/pipeline.yaml`
    + AWS CodeCommit - Git repository
    + AWS CodeBuild - Deployment tool 
    + AWS CodePipeline - Orchestrates pipeline and listen for new commits in CodeCommit
   
