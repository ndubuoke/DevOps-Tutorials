FROM node:10 AS build

WORKDIR /app

COPY . .

RUN yarn build

FROM nginx:alpine

WORKDIR /usr/share/nginx/html

COPY --from=build /app/build .

CMD ["nginx"]
