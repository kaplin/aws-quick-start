# Using CloudFormation Template

## Prereqisites 
* AWS CLI 2 https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html
* GIT https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html?icmpid=docs_acc_console_connect_np#setting-up-gc-install-git 

## Create CodeCommit Repo

```
aws2 cloudformation create-stack --stack-name aws-demo-infrastructure --template-body "`cat infrastructure.yaml`"
```

# Manual Steps
Template and documentation on how to create full-stack serverless web app with CI/CD on AWS

- [ ] Create CodeCommit Repository https://us-west-2.console.aws.amazon.com/codesuite/codecommit/repository/create?region=us-west-2 
- [ ] Create IAM User with AWSCodeCommitFullAccess policy:
￼
- [ ] Install GIT https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html?icmpid=docs_acc_console_connect_np#setting-up-gc-install-git 
- [ ] Get IAM user creds as shown here https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html?icmpid=docs_acc_console_connect_np#setting-up-gc-iam 
- [ ] $ git clone https://git-codecommit.us-west-2.amazonaws.com/v1/repos/aws.demo
