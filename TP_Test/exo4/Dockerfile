FROM nginx:latest

COPY fichier.zip /usr/share/nginx/html/

RUN apt-get update && \
    apt-get install -y unzip && \
    unzip /usr/share/nginx/html/fichier.zip -d /usr/share/nginx/html/ && \
    rm /usr/share/nginx/html/fichier.zip
