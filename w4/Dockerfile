#Crate multi stage docker
#Build stage

FROM golang:1.21.1-alpine as builder

#Set the working directory
WORKDIR /app

#Build the app
RUN go build -o myapp

#use a smaller image to reduce the size of the final container
FROM alpine:latest

#Set working Directory
 
WORKDIR /root/

#Copy the binary from the builder stage
COPY --from=builder /app/myapp .

#Execute the app
CMD ["./myapp"]