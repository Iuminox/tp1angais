FROM node:16
ENV HTTPS_PROXY https://192.168.2.7:3128
ENV HTTP_PROXY http://192.168.2.7:3128
run npm config set proxy http://192.168.2.7:3128
run npm config set https-proxy http://192.168.2.7:3128

# Create app directory
WORKDIR /app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .
RUN npm install --production
 
CMD [ "node", "src/index.js" ]
