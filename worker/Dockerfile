FROM node:latest
WORKDIR /app
RUN apt-get update  && apt-get install -y git
RUN git clone https://github.com/handipradana/nodejsbasic.git .
ARG DB_HOST
ENV DB_HOST=database-1.cluster-cs5pp3kg7wkf.us-east-1.rds.amazonaws.com
ARG DB_USER
ENV DB_USER=admin
ARG DB_PASSWORD
ENV DB_PASSWORD=ambatukam
ARG DB_DATABASE
ENV DB_DATABASE=crud_db
RUN npm install -g pm2
RUN npm install 
EXPOSE 8000
CMD ["pm2-runtime","npm","--","run","start-prod"]