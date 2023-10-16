# docker-cheatsheet

**docker ps** - list all running containers along with details like ports, container ID, image name etc.
**docker-compose up -d [image name]**, it will run service as in deamon mode(Background)
**docker-compose stop [image name]**, stop a service
**docker-compose rm [image_name]** , rm a service

**docker build -t tagName .** (Create a build of a repository, you can make it up by going into the docker-compose.yml file directoy using above command (docker-compose up -d [image_name])

**docker images** , list all your images 

getting kafka UI in your server
**docker run -d --network=ones-network -p 8090:8080 -e DYNAMIC_CONFIG_ENABLED=true provectuslabs/kafka-ui**

## For Logs
**docker logs [container_id]** - show logs of your applocation till last breakpoint
**docker logs [container_id] --follow** , show logs of your service, it will not terminate until you do **CMND + C**
**docker logs [container_id] --tail=N** , it will show last N logs
