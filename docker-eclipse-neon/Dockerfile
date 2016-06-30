FROM docker-orcale-java8

RUN apt-get install tar -y

#Install eclipse neon
Run wget http://ftp.acc.umu.se/mirror/eclipse.org/technology/epp/downloads/release/neon/R/eclipse-java-neon-R-linux-gtk-x86_64.tar.gz -O /tmp/eclipse.tar.gz -q
RUN \
    echo 'Installing eclipse' && \
    tar -xf /tmp/eclipse.tar.gz -C /opt && \
    rm /tmp/eclipse.tar.gz

RUN sed -i s/--launcher.appendVmargs/--launcher.GTK_version\\n2\\n--launcher.appendVmargs/g /opt/eclipse/eclipse.ini
