FROM node:10-alpine
ENV NODE_ENV=production
ENV CONNECTON_STRING=postgresql://postgres://user_id:admin@db/postgres_db
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production --silent && mv node_modules ../
COPY api api
RUN chown -R node /usr/src/app
USER node
CMD ["node", "index.js"]
