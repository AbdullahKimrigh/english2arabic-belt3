FROM node:10-alpine
ENV CONNECTON_STRING=postgres://user_id:admin@db/postgres_db
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install
COPY . . 
CMD ["node", "index.js"]
