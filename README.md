# execute-in-ubuntu

Mount the current directory and run a linux command on a file.

Main usecase is to check or build debian packages from a non-debian system, for example a Mac.

## Examples:

### list the current directory
`docker run --rm -it -v $PWD:/app execute-in-ubuntu ls -l`

### install a debian package and examine its contents in a bash
`docker run --rm -it -v $PWD:/app execute-in-ubuntu dpkg -i your-package-in-current-folder.deb; bash`

### run a bash to do your steps manually
`docker run --rm -it -v $PWD:/app execute-in-ubuntu bash`


## Alias

You can also create an alias to use this easier:
`alias ubuntu="docker run --rm -it -v $PWD:/app execute-in-ubuntu"`

Starting a bash would then be
`ubuntu bash`