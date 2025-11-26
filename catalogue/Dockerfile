from node:20
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
ENV mongo="true" \
    mongo= "mongodb://mongodb:27017/catalogue"
CMD ["node", "server.js"]
