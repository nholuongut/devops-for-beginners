FROM node:8.16.1-alpine
LABEL maintainer="Nho Luong <luongutnho@hotmail.com>"
WORKDIR /app
COPY . /app
RUN npm install
EXPOSE 5000
CMD node index.js

#ENTRYPOINT ["node", "index.js"]
#COPY package.json /app
