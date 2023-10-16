# docker-cheatsheet


- `docker ps`: List all running containers along with details like ports, container ID, image name, etc.
- `docker-compose up -d [image name]`: Run a service as a daemon in the background.
- `docker-compose stop [image name]`: Stop a service.
- `docker-compose rm [image_name]`: Remove a service.
- `docker build -t tagName .`: Create a Docker image with a specified tag name based on the current directory (where a Dockerfile is located).
- `docker images`: List all your Docker images.

To get Kafka UI in your server:

- `docker run -d --network=ones-network -p 8090:8080 -e DYNAMIC_CONFIG_ENABLED=true provectuslabs/kafka-ui`: Run a Kafka UI container in daemon mode with network settings, port mapping, and environment variables.

## For Logs
Here are your additional Docker log commands presented in markdown format:

- `docker logs [container_id]`: Show logs of your application up to the last breakpoint.
- `docker logs [container_id] --follow`: Show logs of your service continuously; it will not terminate until you manually interrupt it using `Ctrl + C`.
- `docker logs [container_id] --tail=N`: Show the last N logs from the container's log output.
