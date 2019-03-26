## Purpose

This is a collection of CloudFormation Templates.

## Source code structure

```bash
├── code_pipeline
│   └── pipeline.yaml                       <-- Cloudformation to create entire pipeline
├── buildspec.yml                           <-- CodeBuild spec                           
```
## Cloudformation template

CloudFormation will create the following resources:

* `code_build/pipeline.yaml`
    + AWS CodeCommit - Git repository
    + AWS CodeBuild - Deployment tool 
    + AWS CodePipeline - Orchestrates pipeline and listen for new commits in CodeCommit
    
* ##### TODO:
    + Amazon SNS Topic - CodeBuild Notification via subscribed email
    + Amazon Cloudwatch Events Rule - Custom or CodeBuild Event that will trigger SNS upon build completion
    + Amazon Lambda - Use Lambda to sent notification instead of Cloudwatch Event