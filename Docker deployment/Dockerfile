FROM continuumio/anaconda3:4.4.0
#FROM ubuntu:latest
#FROM python:3.8-slim-buster
MAINTAINER ARKA GHOSH, arka.ghosh@se.com
EXPOSE 8000
RUN apt-get update && apt-get install -y apache2 \
    apache2-dev \   
    vim \
 && apt-get clean \
 && apt-get autoremove \
 && rm -rf /var/lib/apt/lists/*
WORKDIR /var/www/fastapi_predict_api/
COPY ./fastapi_demo /var/www/fastapi_predict_api/
RUN pip install -r requirements.txt
CMD ["python", "./fastapi_predict_api.py"]
