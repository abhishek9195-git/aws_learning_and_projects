# 1. Installations

1.1 Install kubectl


1.2 Install eksctl 
```
> brew tap aws/tap
```
```
> brew install aws/tap/eksctl
```


1.3 Install aws cli
```
> curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
> sudo installer -pkg AWSCLIV2.pkg -target /
> aws --version
```


# 2. Configure
// Create access key and access secret in aws settings > credential manager > create access key
```
> aws configure
```
```
> Provide your access key and secret
```


# 3. Create eks cluster
```
> eksctl create cluster --name demo-cluster --region us-east-1 --fargate
```
```
> eksctl delete cluster --name demo-cluster --region us-east-1
```


# 4. Create fargate profile
```
eksctl create fargateprofile \
--cluster demo-cluster-1 \
--region us-east-1 \
--name alb-sample-app \
--namespace game-2048
```
