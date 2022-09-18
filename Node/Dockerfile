FROM node:12.16.3-alpine

# Create app directory
WORKDIR /usr/src/app

COPY package*.json ./

ENV NODE_ENV=production

# Install app dependencies
RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

RUN npm install pm2 -g

EXPOSE 8000

CMD ["pm2-runtime", "src/server.js"]
