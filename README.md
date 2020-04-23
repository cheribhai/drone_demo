# Drone Demo

Drone Demo project to test various types of pipelines with drone.

# Docker Compose Volume

The **compose_volume** directory contains configuration to test the mounting of volume in a docker (compose) running within the drone docker container.

Since we have to mount the host docker socket _/var/run/docker.sock_ on the docker container it means that any volume to be mounted will always refer to paths on the HOST machine and not the parent container.

One way to solve this problem would be to mount a known host directory like _/tmp_ and copy files / directories to be mounted in the nested container to this dir.
