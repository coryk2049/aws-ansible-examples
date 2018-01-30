# vpc-5
Provision an example ALB with 2 AZs.

Path patterns:

+ `<ALB DNS>` = Apache (Default)
+ `<ALB DNS>/[nginx|apache].html` = Nginx / Apache

Tested using Ansible v2.4.x on Ubuntu 16.04

## Prerequisites
1) Make sure to set `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `AWS_DEFAULT_REGION` environment variables in your profile.

2) Ensure key values in `roles/[iam|vpc|ec2|alb]/vars/main.yml` are valid

## Gotchas
1) `ec2.instance_profile_name` commented out in favor of `aws cli` instance profile commands

2) Ansible ALB modules not fully complete so `aws elbv2` commands used as a workaround

## Execute Playbook
`# ansible-playbook playbook.yml`
