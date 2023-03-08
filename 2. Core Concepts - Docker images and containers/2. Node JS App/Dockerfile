### Run container based on image (node.js example)

## Contains setup instructions for docker when we will build our own custom image from a pre-built image (docker hub)

# FROM --> built own image on base image (docker hub)
FROM node

# all commands will be executed inside app folder
WORKDIR /app

# COPY --> which files should go into the image
# copy the dependencies into the app
COPY package.json /app

# After copying all local files, intall all dependencies
RUN npm install

### first dot --> call folder, sub-folders, and files should be copied into the image
### second dot/path --> path inside the image where the files should be stored (inside the app folder).
COPY . /app 

# Expose a port to our local system (for communication with container)
EXPOSE 80

# Start server by executing node command to run server.js file
CMD ["node", "server.js"]


# writing image sha256:712796388293cfc364fc223201095eb363ae475c23f3fd980cc61eae11777b0a


## Each instruction in this file creates a layer in the image (image layer based architecture)