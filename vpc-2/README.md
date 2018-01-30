# vpc-2
Provision a barebone VPC with 1 AZ, 2 subnets, IGW, NGW, group, users, and role.

Tested using Ansible v2.4.x

## Prerequisites
1) Make sure to set `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` environment variables in your profile.

2) Ensure key values in `roles/[iam|vpc]/vars/main.yml` are valid

## Execute Playbook
`# ansible-playbook playbook.yml`
