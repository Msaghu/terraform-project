# Terraform Beginner Bootcamp 2023

##  Semantic versioning :mage:
This project will utilize semantic versioning 
for its tagging.
[Semantic versioning](https://semver.org/)

Given a version number MAJOR.MINOR.PATCH, increment the:

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes
Additional labels for pre-release and build metadata are available as extensions to the **MAJOR.MINOR.PATCH** format.

## Considerations for Linux Distributions

Since this project is built in Ubuntu. We consider checking the Linux Distribution and refactor according to Linux distribution needs.

How to check OS version
```
$ cat /etc/os-release 

PRETTY_NAME="Ubuntu 22.04.5 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.5 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=jammy
```

### Linux permisions and executions
In order to make a file executable , we need to chnage linux permisiions
```sh
chmod u+x ./bin/install_terraform_cli
```


To create a file into a bash script, we use a shebang `#! /usr/bin/env bash`

- For portability and  works for multiple Linux distributions

When executing the bash script we can use the `./` shorthand notification eg
`./bin/install_terraform_cli`.

To ensure that the script run when we launch Gitpod through the gitpod.yml, we use
`source ./bin/install_terraform_cli`

## Installing the Terraform CLI 
When using Terraform to build infrastructure, we need to install it in our environment. 
We follow the instructions listed on the offical Terraform page , to take into account the gpg keyring changes.
[sup]2[sup]

## Refactoring into bash scripts

We create a [bash script](./bin/install_terraform_cli.sh) that automates the installation of Terraform into your environment as a one step process.

- This allows the Gitpod task file to be tidy.
- The file is now portable for other projects.
- It is easier to debug and can be installed manually.

### Github/Gitpod Lifecycle (Before, Init, Command)
We need to be carefiul when 

RESOURCES
1. [Github Flavoured Markdown](https://github.github.com/gfm/)
2. [How to check Linux version](https://www.geeksforgeeks.org/how-to-check-the-os-version-in-linux/)
3. [Installing Terraform on your workspace](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
4. [Linux permissions](https://www.redhat.com/en/blog/linux-file-permissions-explained#:~:text=All%20Linux%20files%20belong%20to,write%2C%20and%20x%20for%20execute.)



