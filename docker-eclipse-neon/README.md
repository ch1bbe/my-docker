docker build -t docker-eclipse-neon .

docker run -it --rm \
       -e DISPLAY=$DISPLAY \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
       docker-eclipse-neon

#Known issue
When running xeyes:

No protocol specified
Error: Can't open display: unix:0

xhost +
