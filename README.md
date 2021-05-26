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

## Acknowledgements
- [A step by step guide to mTLS in Go](https://venilnoronha.io/a-step-by-step-guide-to-mtls-in-go)