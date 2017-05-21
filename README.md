# CloudFormation Examples

These are some very basic raw CloudFormation template examples.  This examples are part of a blog tutorial.


### Tutorial 2

```bash
aws cloudformation create-stack --template-body file://templates/single_instance.yml --stack-name single-instance --parameters ParameterKey=KeyName,ParameterValue=tutorial ParameterKey=InstanceType,ParameterValue=t2.micro
```

### Tutorial 2

```bash
aws cloudformation create-stack --template-body file://templates/single_instance.yml --stack-name --stack-name route53-$(date +%s) --parameters ParameterKey=KeyName,ParameterValue=tutorial ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=HostedZoneName,ParameterValue=sub.tongueroo.com. ParameterKey=Subdomain,ParameterValue=testsubdomain

aws cloudformation create-stack --template-body file://templates/instance_and_route53.yml --stack-name route53-$(date +%s) --parameters file://parameters/instance_and_route53.json
```

