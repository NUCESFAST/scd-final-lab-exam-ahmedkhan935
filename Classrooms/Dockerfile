
FROM node:14


WORKDIR /21i1152_backend

COPY package*.json ./


RUN npm install

COPY . . 


CMD ["node", "index.js"]