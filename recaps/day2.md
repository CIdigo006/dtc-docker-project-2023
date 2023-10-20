This is for the second day of the project. For this portion of things we begin getting exposed to interacting with docker further. On day 1 we went over what docker is and why/how it came about along with its pros and cons (alternative to virtual machines and linux containers that is more lightweight easier to get up and running, having a lot of containers running can become a lot to manage{although tools exist to help with that[kubernetes etc]}), what an image is(executable application that also has details configuring its environment), what a container is(a running instance of an image).

Today we created our own docker image, ran it as a container, and interacted with the container.

We did this by first creating a dockerfile filled with instructions on what we what our image to have.

Then we ran that image thus creating a container and interacted with that container.

While interacting with that container we ran our program we loaded on our image from inside our container.

Then we exited the container, and successfully deleted our image.