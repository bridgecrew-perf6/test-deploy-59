ARG NODE_VERSION="8.10.0"
FROM node:$NODE_VERSION

WORKDIR /app

ADD ./serviceb/package.json /app
RUN set -uex; \
    npm install --production; \
    rm -rf /root/.npm;

ADD ./serviceb /app

USER nobody
CMD ["/usr/local/bin/node", "/app/index.js"]
