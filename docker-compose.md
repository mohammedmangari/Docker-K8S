### Common Docker Compose Commands:

1. **Build the images:** This command builds Docker images defined in your `docker-compose.yml` file.
   ```
   docker compose build
   ```

2. **Start the containers:** Starts the containers defined in your `docker-compose.yml`.
   ```
   docker compose start
   ```

3. **Stop the containers:** Stops the containers defined in your `docker-compose.yml`.
   ```
   docker compose stop
   ```

4. **Build and start containers:** Builds the images and starts the containers in the background.
   ```
   docker compose up -d
   ```

5. **List what's running:** Shows the containers and their status.
   ```
   docker compose ps
   ```

6. **Remove from memory:** Removes the containers, networks, and volumes defined in your `docker-compose.yml`.
   ```
   docker compose rm
   ```

7. **Stop and remove containers:** Stops and removes containers, networks, and volumes.
   ```
   docker compose down
   ```

8. **Get the logs:** Displays the logs of the services/containers.
   ```
   docker compose logs
   ```

9. **Run a command in a container:** Executes a command in a running container.
   ```
   docker compose exec [container] bash
   ```

### Compose v2 (2022) Commands:

10. **Run an instance as a project:** Starts a Compose project with a specific name.
    ```
    docker compose --project-name projName up -d
    ```

    - Alternatively, you can use the shortcut option to set the project name:
    ```
    docker compose -p projName up -d
    ```

11. **Copy files from a container:** Copies files from a container to the host machine.
    ```
    docker compose cp [ContainerID]:[SRC_PATH] [DEST_PATH]
    ```

12. **Copy files to a container:** Copies files from the host machine to a container.
    ```
    docker compose cp [SRC_PATH] [ContainerID]:[DEST_PATH]
    ```

These commands can be useful for managing Docker Compose services and containers in various scenarios. Just replace `[container]`, `[ContainerID]`, `[SRC_PATH]`, and `[DEST_PATH]` with the appropriate values for your specific use case.