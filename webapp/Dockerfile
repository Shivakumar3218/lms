#here we are taking NOdE to frondenf script and assigned to build as name to use for other base
FROM node:16 AS build
RUN mkdir /frontend
COPY . /frontend
WORKDIR /frontend
RUN npm install
RUN npm run build 

FROM nginx 
COPY --from=build /frontend/dist /usr/share/nginx/html

