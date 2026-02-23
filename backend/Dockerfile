FROM node:18

# create app folder
WORKDIR /app

# copy package files first
COPY package*.json ./

# install dependencies
RUN npm install

# copy rest of code
COPY . .

# expose backend port
EXPOSE 8080

# start server
CMD ["node", "server.js"]