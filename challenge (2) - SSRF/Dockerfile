FROM node:18

WORKDIR /app

COPY src/package*.json ./

RUN npm install

COPY . .

RUN npm install pm2 -g  

EXPOSE 5000

CMD ["pm2", "start", "src/app.js", "src/admin.js", "--no-daemon"]
