FROM node:16
#creating one folder to push all backend files
RUN mkdir /backend
#copy all files in api to backedn with .env also
COPY . /backend
#WORKDIR - it is like cd to go in it
WORKDIR /backend
RUN npm install
RUN npx prisma generate
RUN npx prisma db push
RUN npm run build
EXPOSE 8080 
#exposing port to container 
CMD ["node","build/index.js"]


