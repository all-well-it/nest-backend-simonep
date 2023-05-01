FROM node:18.16.0-alpine

WORKDIR /app

COPY package.json .
RUN npm install

#src folder will be loaded as a volume for hot-reloading
COPY .eslintrc.js nest-cli.json tsconfig.build.json tsconfig.json ./

EXPOSE 3000
#start nestjs in watch mode
CMD [ "npm", "run", "start:dev" ]