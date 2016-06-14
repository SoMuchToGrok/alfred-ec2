# alfred-ec2

An [Alfred](https://www.alfredapp.com) workflow to query for EC2 instances by tag and SSH into the instance using its private IP address. Type `ec2ls` in Alfred to get a list of instances.

## Dependencies
- [iTerm2 3.0+](https://www.iterm2.com/downloads.html) (not backwards compatible)
- zsh shell
- Python executable located at /usr/local/bin/python

## Setup

This script makes use of
[deanishe/alfred-workflow](https://github.com/deanishe/alfred-workflow) and
[boto/boto](https://github.com/boto/boto).

1) Clone this repo in Alfred's workflow directory (typically ~/Documents/Alfred.alfredpreferences/workflows)
```
git clone git@github.com:SoMuchToGrok/alfred-ec2.git ~/Documents/Alfred.alfredpreferences/workflows
```
2) Execute setup.sh to install python dependencies.
```
~/Documents/Alfred.alfredpreferences/workflows/ec2-alfred-workflow/setup.sh
```

To access AWS, it will use the credentials stored under `~/.aws/config`. You
can use the command `awsprofile` in Alfred to select which account to use. Also use
`awsregion` to select the region. Use `awsuser` to select the default user.

When you select an instance, it will start an `iTerm2` session and execute a
ssh command (strict host key checking disabled) using the default user and will try to load a ssh key with the
same name as the session. The applescript can easily be modified as needed.
