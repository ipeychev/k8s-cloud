FROM node:10-stretch-slim

ENV LCP_CONTAINER_ID="autoscaller"

WORKDIR /lcp-container

COPY ./package.json /lcp-container
COPY ./package-lock.json /lcp-container

RUN set -ex && \
    npm install --only=production

COPY . .

CMD [ "npm", "start" ]