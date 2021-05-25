# ecs-python-sample
A simple python flask webapp, dockerized to be run in AWS ECS with Fargate.

## CloudFormation Templates

Setup the network, including a VPC with public and private subnets in two AZs, an ECS cluster, ALBs, NAT GWs, Security Groups and IAM roles.

```shell
aws cloudformation deploy --template ./cloudformation_networking.yml--stack-name ecs-python-sample-network
```

Create a Service and a Task definition in ECS cluster
```shell
aws cloudformation deploy --template ./cloudformation_services.yml --stack-name ecs-python-sample-services
```
