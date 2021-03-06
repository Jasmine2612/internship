# Search dockehub for neo4j
 docker search neo4j

# Pulling a dockerhub
```` bash
docker pull neo4j
````

# Running a neo4J docker
```` bash
docker run \                                        #base command
    --detach                                        # run docker in background
    --name  <container_name>                                  # container name
    --publish=7474:7474 --publish=7687:7687 \       # which port to use <choice>:<default>
    --volume=$HOME/neo4j/data:/data \               # where to store data
    neo4j                                           #what to run
````

# Search dockehub for mongodb
 docker search mongo


```` bash
docker run \
    --detach                                        # run docker in background
    --name  <container_name>                        # container name
    --publish= "27017:27017" \                      # which port to use <choice>:<default>
    --volume= $HOME/mongodb_data/db:/data/db \      # where to store data
    mongo
````

# Search dockehub for postgre

```` bash
docker search postgres
````

```` bash
docker pull postgres
````

```` bash
docker run -d \
    --name some-postgres \
    -e POSTGRES_PASSWORD=mysecretpassword \
    -e PGDATA=/var/lib/postgresql/data/pgdata \
    -v /custom/mount:/var/lib/postgresql/data \
    postgres
    
````
