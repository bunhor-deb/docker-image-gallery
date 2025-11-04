FROM node:15.14-alpine

WORKDIR /app

EXPOSE 3000

COPY package.json package-lock.json ./

RUN npm install --silent 

COPY . ./

RUN mkdir -p /app/node_modules/.cache && \
    chown -R node:node /app

USER node

CMD ["npm", "start"]