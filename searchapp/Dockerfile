FROM mhart/alpine-node:latest

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ENV PATH /usr/src/app/node_modules/.bin:$PATH

COPY package.json /usr/src/app/package.json
RUN yarn

COPY ./public /usr/src/app/public
COPY ./src /usr/src/app/src

CMD ["npm", "start"]