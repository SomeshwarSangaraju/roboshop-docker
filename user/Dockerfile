# FROM node:20.19.6-alpine3.22 AS build
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install


# FROM node:20.19.6-alpine3.22 
# WORKDIR /opt/server
# EXPOSE 8080
# RUN addgroup -S roboshop && adduser -S roboshop -G roboshop && \
#     chown -R roboshop:roboshop /opt/server
# LABEL com.project="roboshop" \
#       createdby="someshwar" \
#       component= "user"     
# ENV MONGO="true" \
#     REDIS_URL='redis://redis:6379' \
#     MONGO_URL="mongodb://mongodb:27017/users"
# COPY --from=build --chown=roboshop:roboshop /opt/server /opt/server
# USER roboshop
# CMD ["server.js"]
# ENTRYPOINT ["node"]


FROM node:20
WORKDIR /opt/server
EXPOSE 8080
COPY package.json .
COPY *.js .
RUN npm install
ENV MONGO="true" \
    REDIS_URL='redis://redis:6379' \
    MONGO_URL="mongodb://mongodb:27017/users" 
CMD ["node", "server.js"]
