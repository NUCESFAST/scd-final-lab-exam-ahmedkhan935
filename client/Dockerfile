FROM node:14 as build

WORKDIR /21i1152_frontend

COPY package*.json ./

RUN npm install

RUN npm install -g serve

COPY . .

RUN npm run build

CMD ["serve", "-s", "-l", "5000", "build"]
