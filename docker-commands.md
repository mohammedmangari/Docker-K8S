# Docker CLI

### Running and Stopping Containers:

1. **Pull an image from a registry:**
   ```
   docker pull [imageName]
   ```

2. **Run containers:**
   ```
   docker run [imageName]
   ```

3. **Run containers in detached mode:**
   ```
   docker run -d [imageName]
   ```

4. **Start stopped containers:**
   ```
   docker start [containerName]
   ```

5. **List running containers:**
   ```
   docker ps
   ```

6. **List running and stopped containers:**
   ```
   docker ps -a
   ```

7. **Stop containers:**
   ```
   docker stop [containerName]
   ```

8. **Kill containers:**
   ```
   docker kill [containerName]
   ```

9. **Get image info:**
   ```
   docker image inspect [imageName]
   ```

### Building Images:

10. **Build an image using a Dockerfile located in the same folder:**
    ```
    docker build -t [name:tag] .
    ```

11. **Build an image using a Dockerfile located in a different folder:**
    ```
    docker build -t [name:tag] -f [fileName]
    ```

12. **Tag an existing image:**
    ```
    docker tag [imageName] [name:tag]
    ```

### Cleaning Up:

13. **Remove stopped containers:**
    ```
    docker rm [containerName]
    ```

14. **Remove all stopped containers:**
    ```
    docker rm $(docker ps -a -q)
    ```

15. **List images:**
    ```
    docker images
    ```

16. **Delete an image:**
    ```
    docker rmi [imageName]
    ```

17. **Remove all images not in use by containers:**
    ```
    docker system prune -a
    ```

### Limits:

18. **Set maximum memory for a container:**
    ```
    docker run --memory="256m" nginx
    ```

19. **Set maximum CPU shares for a container:**
    ```
    docker run --cpus=".5" nginx
    ```

### Attaching Shells:

20. **Attach a shell to a container (Linux):**
    ```
    docker run -it nginx -- /bin/bash
    ```

21. **Attach PowerShell to a container (Windows):**
    ```
    docker run -it --microsoft/powershell:nanoserver pwsh.exe
    ```

22. **Attach to a running container:**
    ```
    docker container exec -it [containerName] --bash
    ```

These commands cover a wide range of Docker CLI operations, from managing containers to building images and performing maintenance tasks. Make sure to replace `[imageName]`, `[containerName]`, `[name:tag]`, and other placeholders with the actual values when using these commands.