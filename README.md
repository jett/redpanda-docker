These is a docker compose file to spin up a single redpanda broker using instructions from:
https://docs.redpanda.com/docs/get-started/quick-start/?quickstart=docker

### starting it up
`docker compose up -d`

### get info about the cluster
`docker exec -it redpanda-0 rpk cluster info`


### create a topic
`docker exec -it redpanda-0 rpk topic create events`

### produce something to send to the topic
`docker exec -it redpanda-0 rpk topic produce events`
#### enter a message to be sent

### consume the message
`docker exec -it redpanda-0 rpk topic consume events --num 1`

### you can access the local panda by going to
`http://127.0.0.1:8080/`

### cleanup
`docker compose down -v`
