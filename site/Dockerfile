FROM node:17.9-slim

WORKDIR /site

COPY package.json .
COPY yarn.lock .

RUN yarn install

COPY . .

ENV NODE_ENV=production

ENV PORT=8000

EXPOSE 8000

RUN yarn build

CMD ["yarn", "start", "-p", "8000"]
