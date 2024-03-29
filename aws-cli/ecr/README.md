# ECR CLI Cheatsheet

## Docker Login Token

Get the docker login token:

```
$(aws --profile dev ecr get-login --region eu-west-1 --no-include-email | tr -d '\r')
```

One liner to login:

```
$ aws --profile prod ecr get-login-password --region eu-west-1 | docker login --username AWS --password-stdin $ACCOUNT_ID.dkr.ecr.eu-west-1.amazonaws.com
```

## Create Repository

Create a ECR Repository:

```
$ aws --profile dev ecr create-repository --repository-name my-ecr-repo
```
