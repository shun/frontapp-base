FROM node:lts-buster-slim

WORKDIR /home/node

ADD ./vue/.vuerc /home/node
RUN apt update \
    && apt install -y \
        git \
        nginx \
        sudo \
        supervisor \
        whois \
    && rm -rf /var/lib/apt/lists/* \
    && yarn global add \
        @vue/cli

USER node
ARG VUE_CLI_SKIP_DIRTY_GIT_PROMPT=1

RUN vue create frontapp -p mypreset

