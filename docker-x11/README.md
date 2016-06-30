docker build -t docker-x11 .

docker run -it --rm \
       -e DISPLAY=$DISPLAY \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
       docker-x11

#Known issue
When running xeyes:

No protocol specified
Error: Can't open display: unix:0

xhost +
