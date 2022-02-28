FROM node:10

# App directory
WORKDIR /usr/src/app

# Copy package into directory
COPY package*.json ./

# Run library
RUN npm install

# Copy folder up to working directory
COPY . .

EXPOSE 8080

CMD ["node", "index.js"]