# Building images, container and volumes in a Windows Machine
# Topics covered here: Images, Containers, Volumes, Bind Mounts, ENV variables, ARG variables

FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ARG DEFAULT_PORT=80 

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

# VOLUME ["/app/feedback"]

CMD [ "node", "server.js" ]


# docker build -t feedback-node:env .
# docker run -d --rm -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "%cd%":/app -v /app/node_modules -v /app/temp feedback-node:env


