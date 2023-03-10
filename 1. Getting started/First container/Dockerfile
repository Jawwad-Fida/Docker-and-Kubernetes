# Base Image
FROM node:14

# dir for that file system in container
WORKDIR /app

COPY package.json .

# install all dependencies
RUN npm install

COPY . .

# expose port to the outside world (To reach port outside the container)
EXPOSE 3000 

CMD [ "node", "app.mjs" ]

# writing image sha256:bda291f26963b6b7ff73c373614a60f24cbc933b8bb351e7e932fb5477ed97e3
