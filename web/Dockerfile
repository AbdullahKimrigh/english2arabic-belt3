FROM node:10-alpine
ENV NODE_ENV=production
ENV API_ENDPOINT=API_URL=http://api:3001/data
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production --silent && mv node_modules ../
COPY . .
EXPOSE 3000
RUN chown -R node /usr/src/app
RUN chmod 777 node /usr/src/app
USER node
CMD ["node", "index.js"]
