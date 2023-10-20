This is from the second day of the project. For this portion of things we begin getting exposed to interacting with docker further. On day 1 we went over what docker is and why/how it came about along with its pros and cons (alternative to virtual machines and linux containers that is more lightweight easier to get up and running, having a lot of containers running can become a lot to manage{although tools exist to help with that[kubernetes etc]}), what an image is(executable application that also has details configuring its environment), what a container is(a running instance of an image)


On day 2 we work to create a simple docker image that will allow us to run a lisp repl application. 

To do this we have to configure our dockerfile and write down the appropriate instructions to create the image we want to, then we run our image in interactive mode thus allowing us to shell into the container that is created for that instance of the image, while in the container we run the lisp repl app that we added to our image. 

This allows us to see how to simply run an app using docker. 

In the dockerfile that has been uploaded, comment out the CMD instruction otherwise the CMD will run and you'll be see the "hello world" display. If you still wnat to run it this way skip to the section about building the image

Information about the dockerfile and what is happening can be found in the comments located in the file

To build the image, Open the terminal and navigate to the location of the docker file. Once there run the following command <docker build -t lisp .> this builds the docker image, assigns it the name of lisp, and builds the docker image with the information found in the dockerfile in the pwd which is why we use <.> if we want we can write the path to the specific dockerfile we want to work with when executing the command

Afterwards, run <docker image ls> to get the image id for the image we just built. It should be named 'lisp' and the image id will be assigned at random. Copy this image id

Next, in a separate terminal run the following command <docker run -it [image id]> and the image will start running and we will be located on the command line of the container. We can use <docker run [image id]> to run the image as well but we won't be operating within the container. We'd just run the image thus creating a container and that'll be it. But by running it with -it we are stating we want to interact with the container and as such we'll be within the container machine.

While there we run <sbcl>  which runs the lisp repl while we're inside our container. From there we can interact with the repl as we would like. If we want to run hello world we do the following (format t "hello, world")

After we're done playing around inside of the container, we can press ctrl+d once to exit lisp repl, press ctrl+d a second time to exit the container. Once we close the container, the container will delete itself as we did not tell it to run after we exit