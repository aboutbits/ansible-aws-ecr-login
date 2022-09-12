Ansible AWS ECR Login Role
==========================

Login to AWS ECR role.

## Role Variables

- `aws_ecr_login_repository`: The AWS ECR repository

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        ansible-aws-ecr-login
      vars:
        aws_ecr_login_repository: xxx.dkr.ecr.eu-west-1.amazonaws.com
```

## Versioning

In order to have a verioning in place and working, create leightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag 1.0
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d 1.0
git push origin :refs/tags/1.0
git tag 1.0
git push --tags
```
