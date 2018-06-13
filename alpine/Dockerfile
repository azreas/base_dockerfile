FROM alpine:3.7
MAINTAINER azreas <azreas.x@gmail.com>

# Install base packages
RUN apk update && apk add curl bash tree tzdata \
    && cp -r -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo -ne "Alpine Linux 3.7 image. (`uname -rsv`)\n" >> /root/.built

# Install glibc
RUN apk --no-cache add ca-certificates wget
RUN wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://raw.githubusercontent.com/sgerrand/alpine-pkg-glibc/master/sgerrand.rsa.pub
RUN wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.27-r0/glibc-2.27-r0.apk
RUN apk add glibc-2.27-r0.apk
RUN rm -f glibc-2.27-r0.apk

# Custom aliases
RUN alias l='ls -a' \
    && alias ll='ls -l' \
    && alias la='ls -la' 

# Define bash as default command
CMD ["/bin/bash"]
