ARG NODE_VERSION="8.10.0"
FROM node:$NODE_VERSION

WORKDIR /app

ADD ./servicea/package.json /app
RUN set -uex; \
    npm install --production; \
    rm -rf /root/.npm;

ADD ./servicea /app

USER nobody
CMD ["/usr/local/bin/node", "/app/index.js"]
