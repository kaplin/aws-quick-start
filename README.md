# Using CloudFormation Template

## Prereqisites 
* [AWS CLI 2](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
* [GIT](https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html?icmpid=docs_acc_console_connect_np#setting-up-gc-install-git)

## Create CodeCommit Repo

Create infrastructure

```
aws2 cloudformation deploy --stack-name aws-demo-infrastructure --template-file infrastructure.yaml
```

Get your repo URL
```
aws2 codecommit get-repository --repository-name aws-quick-start-app --query repositoryMetadata.cloneUrlHttp --output text
```

Access your app Git repo (read more about git credentials helper [here](https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-https-unixes.html#setting-up-https-unixes-credential-helper))
```
git config --global credential.helper '!aws codecommit credential-helper $@'
git config --global credential.UseHttpPath true
git clone <repo_url>
```

# Manual Steps
Template and documentation on how to create full-stack serverless web app with CI/CD on AWS

- [ ] Create CodeCommit Repository https://us-west-2.console.aws.amazon.com/codesuite/codecommit/repository/create?region=us-west-2 
- [ ] Create IAM User with AWSCodeCommitFullAccess policy:
￼
- [ ] Install GIT https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html?icmpid=docs_acc_console_connect_np#setting-up-gc-install-git 
- [ ] Get IAM user creds as shown here https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html?icmpid=docs_acc_console_connect_np#setting-up-gc-iam 
- [ ] $ git clone https://git-codecommit.us-west-2.amazonaws.com/v1/repos/aws.demo
