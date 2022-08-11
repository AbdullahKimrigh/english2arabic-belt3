FROM node:10-alpine
ENV NODE_ENV=production
ENV CONNECTON_STRING=5432
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production --silent && mv node_modules ../
COPY . .
# RUN chown -R node /usr/src/app
# USER node
CMD ["node", "index.js"]
