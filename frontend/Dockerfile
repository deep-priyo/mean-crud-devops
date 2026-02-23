# Step 1: Build Angular app
FROM node:18 as build

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# Step 2: Serve Angular using Nginx
FROM nginx:latest

COPY --from=build /app/dist/angular-15-crud /usr/share/nginx/html
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
