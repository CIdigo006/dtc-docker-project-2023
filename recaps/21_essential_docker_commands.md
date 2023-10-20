1. **Docker version**
   - Function: Check the installed Docker version.
   - Example: `docker --version`

2. **Docker search**
   - Function: Search for images on Docker Hub.
   - Example: `docker search MySQL`

3. **Docker pull**
   - Function: Pull an image from Docker Hub.
   - Example: `docker pull MySQL`

4. **Docker run**
   - Function: Create a container from an image.
   - Example:
     ```sh
     docker run -it --env MYSQL_ROOT_PASSWORD=my-secret-pw --detach mysql
     ```
   - Additional Information:
     - The `--detach` option runs the container in the background.
     - The `--env` option is used to set environment variables.
     - The `-it` option allocates a pseudo-TTY and keeps the standard input open for an interactive session.
        - The 'i' stands for interactive and keeps the container input open even if the container is not attached to a terminal
        - The 't' allows the container's command line to be interactive and without it you might not see the input/output of the container

5. **Docker ps**
   - Function: List running containers.
   - Example: `docker ps`

6. **Docker stop**
   - Function: Stop a container by name or ID.
   - Example: `docker stop f8c52bedeecc`

7. **Docker restart**
   - Function: Restart a stopped container.
   - Example: `docker restart f8c52bedeecc`

8. **Docker kill**
   - Function: Stop a container immediately.
   - Example: `docker kill 09ca6feb6efc`

9. **Docker exec**
   - Function: Access a running container.
   - Example:
     ```sh
     docker exec -it test_db bash
     mysql -uroot -pmy-secret-pw
     SHOW DATABASES;
     ```
   - Additional Information:
     - You need to provide the name or ID of the container (e.g., `test_db`).
     - The `-i` and `-t` options are used to access the interactive mode, allowing you to run commands inside the container.

10. **Docker login**
    - Function: Log in to Docker Hub.
    - Example: `docker login`

11. **Docker commit**
    - Function: Save changes to a new image.
    - Example:
      ```sh
      docker commit 09ca6feb6efc greatlearning/httpd_image
      ```
   - Additional Information:
     - `greatlearning` is the username on Docker Hub.
     - `httpd_image` is the image name for the edited container.

12. **Docker push**
    - Function: Upload an image to Docker Hub.
    - Example:
      ```sh
      docker push greatlearning/httpd_image
      ```
   - Additional Information:
     - The "push" refers to the repository [docker.io/greatlearning/httpd_image].
     - This example pushes the image `greatlearning/httpd_image` to Docker Hub.

13. **Docker network**
    - Function: Manage Docker networks.
    - Example: `docker network ls`
    - Additional Information:
      - Docker network commands in lowercase:
        - `connect`: Connect a container to a network.
        - `disconnect`: Disconnect a container from a network.
        - `create`: Create a network.
        - `ls`: List all networks.
        - `inspect`: Display detailed information on one or more networks.
        - `prune`: Remove all unused networks.
        - `rm`: Remove one or more networks.

14. **Docker history**
    - Function: Check the history of a Docker image.
    - Example: `docker history httpd`
    - Additional Information: Displays a list of commands and changes that led to the creation of the image.

15. **Docker rmi**
    - Function: Remove a Docker image.
    - Example: `docker rmi eb0e825dc3cf`

16. **Docker ps -a**
    - Function: List all containers (running and stopped).
    - Example: `docker ps -a`

17. **Docker copy**
    - Function: Copy a file from a container to the local system.
    - Example: `sudo docker cp 09ca4feb7tfc:/usr/local/apache2/logs/httpd.pid /home/greatlearning/`
    - Additional Information:
      - Use `sudo` to execute with superuser privileges.
      - The file is copied from the container to the local directory.
      - Verify the copy using the `ls` command.

18. **Docker logs**
    - Function: View logs of a specific container.
    - Example: `docker logs 09ca6feb6efc`

19. **Docker build**
    - Function: Build an image from a Dockerfile.
    - Example:
      ```sh
      docker build -t my-custom-image:1.0 /path/to/Dockerfile-directory
      ```
   - Additional Information:
     - Use `-t` to tag the image.
     - Specify the path to the directory containing the Dockerfile.

20. **Docker volume**
    - Function: Create a Docker volume for data storage.
    - Example:
      ```sh
      docker volume create
      docker volume ls
      ```
   - Additional Information:
     - Create a volume using the first command.
     - Check the created volume using the second command.

21. **Docker logout**
    - Function: Log out of Docker Hub.
    - Example: `docker logout`