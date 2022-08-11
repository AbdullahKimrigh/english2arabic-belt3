FROM node:10-alpine
ENV API_URL=http://api:3001/data
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "index.js"]
