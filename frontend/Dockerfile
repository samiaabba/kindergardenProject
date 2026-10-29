# Use Node to build the React application
FROM node:22-bookworm-slim AS build

WORKDIR /app

# Install dependencies
COPY package.json package-lock.json ./
RUN npm ci

# Copy the code and build the website
COPY . .
RUN npm run build

# Use Nginx to serve the built website
FROM nginx:1.28-alpine

COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]