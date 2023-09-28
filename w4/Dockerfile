#Crate multi stage docker
#Build stage

FROM golang:1.21.1-alpine as builer

#Set the working directory
WORKDIR /app

#Buil the app
RUN go build -o myapp