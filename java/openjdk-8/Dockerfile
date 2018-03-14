FROM openjdk:8-alpine

# Install base packages
RUN apk update && apk add curl bash tree tzdata \
    && cp -r -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo -ne "Alpine Linux 3.7 image. (`uname -rsv`)\n" >> /root/.built
    
# Custom aliases
alias l='ls -a'
alias ll='ls -l'
alias la='ls -la'
