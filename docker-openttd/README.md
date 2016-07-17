#Build
docker build -t docker-openttd .

#Run container
docker run -it --rm \
       -e DISPLAY=$DISPLAY \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
       -v ~/.openttd/save/:/root/.openttd/save/ \
       docker-openttd

#Run container with mounted save folder
docker run -it --rm \
       -e DISPLAY=$DISPLAY \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
       -v ~/.openttd/save/:/root/.openttd/save/ \
       docker-openttd

#Known issue
When running xeyes:

No protocol specified
Error: Can't open display: unix:0

xhost +
