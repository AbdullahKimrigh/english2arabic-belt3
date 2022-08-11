FROM node:10-alpine
ENV CONNECTON_STRING=postgres://postgres:postgres@db/postgres_DB
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install
COPY . . 
CMD ["node", "index.js"]
