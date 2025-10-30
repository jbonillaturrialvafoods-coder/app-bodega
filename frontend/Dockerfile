# Frontend Dockerfile - React + Vite (build and serve with nginx)
FROM node:18 as build

WORKDIR /app
COPY src/frontend/package.json ./
RUN npm install
COPY src/frontend/ ./
RUN npm run build || (echo 'No build script found; using dev server' && exit 0)

FROM nginx:stable-alpine
COPY --from=build /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
