FROM node:18.19.1-alpine3.19
EXPOSE 8080
RUN addgroup -S sahashop && adduser -S sahashop -G sahashop
WORKDIR /opt/server
RUN chown sahashop:sahashop /opt/server
USER sahashop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]