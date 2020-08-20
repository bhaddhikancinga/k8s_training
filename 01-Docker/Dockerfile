FROM node:alpine3.10

RUN npm i -g ts-node typescript

RUN echo "hello world"

WORKDIR /app

COPY . .

EXPOSE 8000

CMD ["ts-node", "index.ts"]