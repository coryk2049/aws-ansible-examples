# vpc-4
Provision an example classic ELB with 2 AZs.

Hit `<ELB DNS>` to get either `[nginx|apache]` welcome page.

Tested using Ansible v2.4.x on Ubuntu 16.04

## Prerequisites
1) Make sure to set `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `AWS_DEFAULT_REGION` environment variables in your profile.

2) Ensure key values in `roles/[iam|vpc|ec2|elb]/vars/main.yml` are valid

## Gotchas
1) `ec2.instance_profile_name` commented out in favor of `aws cli` instance profile commands

2) Proxy protocol enabled via `aws elb create-load-balancer-policy`

## Execute Playbook
`# ansible-playbook playbook.yml`
