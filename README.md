# Extended-API-Server


## To generate certificates
```bash
  openssl req -newkey rsa:2048 \
              -new -nodes -x509 \
              -days 3650 \
              -out cert.pem \
              -keyout key.pem \
              -subj "/C=US/ST=California/L=Mountain View/O=Your Organization/OU=Your Unit/CN=localhost" \
              -addext 'subjectAltName=DNS:localhost'
```

##To run the server:
```bash
go  run -v server.go
```

##To run the client on a different instance of the terminal
```bash
go  run -v client.go
```

## Acknowledgements
- [A step by step guide to mTLS in Go](https://venilnoronha.io/a-step-by-step-guide-to-mtls-in-go)