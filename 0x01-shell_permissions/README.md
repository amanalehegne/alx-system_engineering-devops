## Shell Permissions
This directory contains various shell commands to manipulate different shell permissions.

All scripts start with #!/bin/bash

### Change my user ID to betty
```bash
su betty
```
### Print effective user id of current user
```bash
whoami
```
### Print all the groups that current user is part of
```bash
groups
```
### Change owner of the file hello to the user betty
```bash
chown betty hello
```
### Create empty file called hello
```bash
touch hello
```
### Add execute permissions to owner of file hello
```bash
chmod u+x hello
```
### Add execute permissions to the owner and the group owner and read permission to other users to hello
```bash
chmod u+x,g+x,o+r hello
```
### Add execute permissions to everyone on file hello
```bash

```
### Give owner and group no permissions and group all permissions
```bash

```
### Everybody!
```bash
chmod a+X *
```
### James Bond
```bash
chmod 007 hello
```
### John Doe
```bash
chmod 753 hello
```
### Look in the mirror
```bash
chmod --reference=olleh hello
```
### Directories
```bash
chmod a+X *
```
### More directories
```bash
mkdir -m 751 ./my_dir
```
### Change group
```bash
chgrp school hello
```
