FROM node:16-alpine

ARG NODE_ENV=production
ENV NODE_ENV=${NODE_ENV}

WORKDIR /opt/
COPY package.json ./
ENV PATH /opt/node_modules/.bin:$PATH

# RUN yarn config set network-timeout 600000 -g
# RUN yarn install
RUN npm i

WORKDIR /opt/app
COPY ./ .
RUN npm run build

EXPOSE 1337
CMD ["npm", "start"]
