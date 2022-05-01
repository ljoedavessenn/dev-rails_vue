FROM node:lts-alpine
WORKDIR /app

# copy both 'package.json' and 'package-lock.json' (if available)
COPY package*.json ./

# install project dependencies
RUN yarn install

# copy project files and folders to the current working directory (i.e. 'app' folder)
COPY . ./

# # build app for production with minification
# RUN npm run build

EXPOSE 3000
CMD [ "npm", "run", "dev" ]
