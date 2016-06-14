# ec2-alfred-workflow

An [Alfred](https://www.alfredapp.com) workflow to query for EC2 instances and get its private ip. Type `ec2ls` on
Alfred to get a list of instances. Type some query text to filter the instances
by tag name.

To access AWS, it will use the credentials stored under `~/.aws/config`. You
can use the command `awsprofile` on Alfred to select which account to use. Also
`awsregion` to select the region. Use `awsuser` to select the default user.

When you select an instance, it will start an `iTerm2` session and execute a
ssh command using the default user and will try to load a ssh key with the
same name as the session. This has been tested with iTerm 2 3.0+. 

## Setup

This script makes use of
[deanishe/alfred-workflow](https://github.com/deanishe/alfred-workflow) and
[boto/boto](https://github.com/boto/boto).

To setup, go to the workflow directory and execute the script `setup.sh`.
