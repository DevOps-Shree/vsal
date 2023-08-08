FROM node:16-alpine

WORKDIR /VSAL-lab-website/


COPY package*.json ./

COPY . ./

RUN npm install

RUN npm run build

RUN npm i -g pm2

EXPOSE 3000

CMD ["pm2-runtime", "start", "npm", "--", "start"]
