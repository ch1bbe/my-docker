docker build -t docker-orcale-java7 .

docker run -it --rm \
       -e DISPLAY=$DISPLAY \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
       docker-orcale-java7

#Known issue
When running xeyes:

No protocol specified
Error: Can't open display: unix:0

xhost +
