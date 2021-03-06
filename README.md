# alpine-tmux
This is a simple Docker image containing `tmux` and `psql`.

## Build it
Run `./build` to get an image.

## Use it
Start a server with `docker run -ti sduckett/alpine-tmux:latest /usr/bin/tmux
new-session -s fun-and-profit`. `tmux` in a Docker environment is a little
strange; the server will probably exit when there are no clients connected. You
can detach from the docker container with `C-p C-q` (by default). Taking a look
at `docker ps`, you should still see the image running.

Connect to the running container with `docker exec -ti $CONTAINER_ID tmux
attach`, where the `CONTAINER_ID` matches your worldview, and if you're doing
multiple sessions, your session of choice.
