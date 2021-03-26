#Based on formerly used docker image: softandbyte/docker_newman
#Changes: node 8 => node 14 / newman 4.5.7 => 5.2.2

FROM mhart/alpine-node:14

# Set newman version
ENV NEWMAN_VERSION 5.2.2

RUN apk update \
    && apk upgrade \
    && apk add openjdk8 bash \
    && npm install newman --global \
    && rm -rf /var/cache/apk/*
    
# Install newman
RUN npm install -g newman@${NEWMAN_VERSION};