FROM node:17-alpine3.14

WORKDIR /usr/nodeapp

COPY ./package.json ./

RUN npm install

COPY ./ ./

CMD ["npm", "start"]