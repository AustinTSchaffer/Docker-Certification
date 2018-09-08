# Docker CLI

Please note, that depending on your setup, you may need to put sudo in front
of all of these commands. Also, all of these 

## Docker `<command>` vs Docker `<management-command> <command>`

Docker has TONS of commands. So many, that the Docker team was running into name
conflicts with the list of commands. The old format of running docker commands
(`docker <command>`) still works for backwards compatibility reasons, but the
new way to run commands is to run them through the appropriate management
command. For example, `docker run` is the exact same command as
`docker container run`.

## Docker Information

```bash
# Get some basic information about Docker
docker version

# Get more information about Docker
docker info
```

Both of these commands will verify that

1. Docker is installed
2. The Docker daemon
3. You have root permissions or are part of the docker unix group

Both of these commands talk directly with the Docker daemon, with the info
command outputting more in-depth information about your Docker environment and
setup.


## Docker Containers

Creating a new container.

```bash
# Spin up a new container from an image
docker container run ...

# ... detach and run in background
docker container run -d ...

# ... map ports to host machine
docker container run --publish "(host machine port)":"(container port)" ...
```

Container Management

```bash
# Stop/Delete a container
docker container stop
docker container rm

# View running containers
docker container ls
# View all containers
docker container ls -a

# Cat/Follow the logs generated by a container
# Includes options for follow, tail, and head. 
docker container logs

# Show the processes running in the specified container
# Can only do one container at a time. Some options can be
# given to the command.
docker container top
```
