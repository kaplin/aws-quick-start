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

```
zip -r -j app.zip app/* && aws2 s3 cp app.zip s3://aws-quick-start
```
