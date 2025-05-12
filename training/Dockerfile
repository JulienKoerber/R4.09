FROM alpine:3.18
RUN apk add --no-cache python3 py3-pip
WORKDIR /app
COPY test.py .
ENTRYPOINT [ "python3", "test.py" ] 