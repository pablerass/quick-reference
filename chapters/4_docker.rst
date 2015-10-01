.. docker

Docker
######

``docker ps``- List containers.
``docker kill`` - Kill container.

Create, start, stop and delete a container.
``docker create <image>``
``docker start <container>``
``docker stop <container>``
``docker rm <container>``

``docker run -i -t <image>`` - Docker create, run and attach docker.
``docker run -d <image>`` - Run docker in ``-d`` detached mode.


``docker rm `docker ps -aq`` - Remove all non running containers. Running
container return an error. Adding ``--force`` option to ``rm`` will delete also
running ones.

``docker port <container> <port>`` - Get container specified port mapping.

``docker build -t <name> <path>`` - Build a Docker image from a ``Dockerfile``.

Docker port mapping
===================

* ``-P`` map all ports from out container using random host ports.
* ``-p <host>:[<host_port>]:<container_port>`` map a container port to an
  specified port of a host.

