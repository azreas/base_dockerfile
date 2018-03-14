FROM alpine:3.7
MAINTAINER azreas <azreas.x@gmail.com>

# Install base packages
RUN apk update && apk add curl bash tree tzdata \
    && cp -r -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo -ne "Alpine Linux 3.7 image. (`uname -rsv`)\n" >> /root/.built

# Custom aliases
RUN alias l='ls -a' \
    && alias ll='ls -l' \
    && alias la='ls -la' 

# Define bash as default command
CMD ["/bin/bash"]