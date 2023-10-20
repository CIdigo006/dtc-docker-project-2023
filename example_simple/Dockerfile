# This is from the assignment for day 2
# Includes descriptions of what the following portions used to write a dockerfile mean
# everythin in all caps is 

FROM ubuntu:20.04
# This portion of things helps create the base image that we will use to create our image

RUN apt update && apt install -y sbcl
# && means execute the first command and only if that's successful then run the second command
# The run command runs what is put infront of it on the command line. This allows us to install different things that 
# will be layered onto and added to our base image that we declared with the FROM command. We can have multiple run statements 
# in a docker file for different. Just like when using python for something we can have multiple libraries 
# required for the program to work

WORKDIR /usr/src
# This sets the working directory to be used when running the container. We essentially run <cd /usr/src> with the WORKDIR
# command and navigate to that directory upon launching the container. When launched in interactive mode and pwd is run
# we get a response of /usr/src

CMD ["/usr/bin/echo", "Hello World"] 

# The next two forms are referred to as the exec form of writing cmds in docker
# cmd instructions in brackets in the form of ["echo", "Hello World"] and no workdir set and hello world prints
# cmd instructions in brackets in the form of ["echo", "Hello World"] and a workdir set and hello world prints

# cmd instructions outside of brackets in the form of "echo", "Hello World" and a workdir set and the cmd does not print
# cmd instructions outside of brackets in the form of "echo", "Hello World" and no workdir set and the cmd does not print

# The next two forms are referred to as the shell form of writing cmds and using that method will invoke a shell
# cmd instructions outside of brackets in the form of echo "Hello World" and no workdir set and hello world prints
# cmd instructions outside of brackets in the form of echo "Hello World" and a workdir set and hello world prints