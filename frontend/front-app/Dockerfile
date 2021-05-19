FROM node:16.0.0-alpine3.13

WORKDIR /usr/src/app

# Install dependencies
COPY ./app/package*.json ./
RUN npm install -g npm && npm install

# Add rest of the client code
COPY ./app/ ./
RUN npm run build

CMD [ "npm", "run", "dev" ]

EXPOSE 3000
