FROM node:7.9-alpine
MAINTAINER Lukas Holzer <office@lukasholzer.com>

#--------------
# Arguments
#--------------
ARG dir
ARG port

#--------------
# Variables
#--------------
ENV HOME_DIR $dir
ENV PORT $port

RUN ls
RUN mkdir -p $HOME_DIR
RUN ls

WORKDIR $HOME_DIR


COPY package.json $HOME_DIR


# Install dependecies
RUN yarn

# Get all the code needed to run the app
COPY . $HOME_DIR

# Expose port 3000 for NGINX
EXPOSE $PORT

# Startup command
CMD yarn start
