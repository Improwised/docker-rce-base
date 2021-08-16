# rce-base
Base image for remote code execution, where all the languages are pre installed.


## Usage
Before using this conatiner image make sure `Docker` has installed on your machine.

First you need to create a `Dockerfile`.
```Dockerfile
FROM improwised/rce-base:latest

WORKDIR /app

# Verify Java, Node, Go, GCC, PHP, and Python installed
RUN javac -version && \
    java -version && \
    node -v && \
    go version && \
    gcc -v && \
    php -v && \
    python -V

# Write your instructions..
```


