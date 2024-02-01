# docker-cheatsheet

- `docker ps`: List all running containers along with details like ports, container ID, image name, etc.
- `docker-compose up -d [image name]`: Run a service as a daemon in the background.
- `docker-compose stop [image name]`: Stop a service.
- `docker-compose rm [image_name]`: Remove a service.
- `docker build -t tagName .`: Create a Docker image with a specified tag name based on the current directory (where a Dockerfile is located).
- `docker images`: List all your Docker images.
- `docker inspect service_ID or service_name`: For checking the current deployed dir on application.

To get Kafka UI in your server:

- `docker run -d --network=ones-network -p 8090:8080 -e DYNAMIC_CONFIG_ENABLED=true provectuslabs/kafka-ui`: Run a Kafka UI container in daemon mode with network settings, port mapping, and environment variables.

## For Logs
Here are your additional Docker log commands presented in markdown format:

- `docker logs [container_id]`: Show logs of your application up to the last breakpoint.
- `docker logs [container_id] --follow`: Show logs of your service continuously; it will not terminate until you manually interrupt it using `Ctrl + C`.
- `docker logs [container_id] --tail=N`: Show the last N logs from the container's log output.

## Other Useful commands

- `lsof -i:<port_number>` , check any operations are running on the port.
- `kill <pid>`, killing a process/operation

## PM2 for running React Frontend 
- `npm install -g pm2`
- `pm2 start npm -- start -- --port 9111`
- `pm2 list`
- `pm2 stop <app_name_or_id>'

## TMUX (running process as session in Background)
- `tmux list-sessions` (for listing all active sessions)
- `tmux kill-session -t my_session_name` (Deleting an active session)
- `tmux new-session -d -s COMMAND` (For creating and running session in detach mode)

## Nano
- `nano filename` - Open file in edit mode.
- `CTRL + O` - it will writeout the file.
- `enter` - Save it
- `CTRL + X` - exit from nano editor.

## Kafka Commands
- `bin/kafka-server-start.sh config/server.properties` - starting zookeeper.
- `bin/kafka-server-start.sh config/server.properties` - starting kafka-server.
- `bin/kafka-topics.sh --list --bootstrap-server localhost:9092` - List of kafka-topics.
- `bin/kafka-topics.sh --create --topic test-topic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1` - Creating a kafka-topic.
- `bin/kafka-topics.sh --delete --topic your-topic --bootstrap-server localhost:9092` - Deleting a topic.
