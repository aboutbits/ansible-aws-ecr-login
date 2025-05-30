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

In order to have a versioning in place and working, create lightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag v2
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d v2
git push origin :refs/tags/v2
git tag v2
git push --tags
```
