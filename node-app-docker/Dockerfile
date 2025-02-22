FROM node:9.9.0 AS builder
RUN git clone https://github.com/kkenan/basic-microservices.git /repo && cd /repo/node-app && npm install

FROM node:9.9.0-alpine
COPY --from=builder /repo/node-app /node-app

CMD ["node", "/node-app/index.js"]


