FROM node:14-alpine

WORKDIR /app

COPY . .

RUN npm install -g pm2
RUN npm install --production --silent

# chạy với UID:GID là 1000:1000
RUN chown -R node:node /app
USER node
# Production
CMD ["pm2-runtime", "ecosystem.config.js", "--env", "production"]