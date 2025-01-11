# mealie-with-tls
## docker-compose.yaml file with instructions on using SSL/TLS


You'll need to either use a service like acme.sh or certbot (letsencrypt) OR you'll need to purchase a certificate.
Using verification methods like email or DNS validation checks will allow you to get a certificate you can use even on an internal IP address.

Create a directory called mealie (or whatever you want to name it)
Make a "data" directory and a "ssl" directory. (eg: `mkdir data ;; mkdir ssl`)
Download the example docker-compose.yaml file, edit it setting the SMTP settings (or comment out) and edit the `TLS_CERTIFICATE_PATH` and `TLS_PRIVATE_KEY_PATH` as appropriate

Your folder should now have a yaml file and two directories:

docker-compose.yaml
*data*
*ssl*

```
docker-compose pull
docker-compose build
docker-compose up -d
```
