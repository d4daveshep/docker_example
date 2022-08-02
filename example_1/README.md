# Docker Simple Example #

This project is a simple example of how to dockerise a python script. \
It includes a couple of dependencies that need to be installed via pip

### To build the docker image ###
Build the docker image tagging it as `python-greeting` and using the current directory \
`docker build -t python-greeting .`

### To run the docker image ###
If no user input is required...\
`docker run python-greeting`\
\
If user input is required we need to use `-i -t` for interactive and psuedo-terminal...\
`docker run -i -t python-greeting`

