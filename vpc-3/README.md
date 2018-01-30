# vpc-3
Provision an example impact level 2 VPC with 3 tier architecture (DMZ / Bastian / Reverse Proxy, Web / App, Database) in a single AZ.

Tested using Ansible v2.4.x on Ubuntu 16.04

## Prerequisites
1) Make sure to set `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `AWS_DEFAULT_REGION` environment variables in your profile.

2) Ensure key values in `roles/[iam|vpc|ec2]/vars/main.yml` are valid

## Gotchas

`ec2.instance_profile_name` commented out in favor of `aws cli` instance profile commands

## Execute Playbook
`# ansible-playbook playbook.yml`
