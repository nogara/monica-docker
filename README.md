# Running Monica using Docker Compose

Based on the [examples](https://github.com/monicahq/docker/tree/main/.examples) from the original Monica [docker repository](https://github.com/monicahq/docker), we are running:

## Services

### App (Monica itself)

Using the [supervisor example](https://github.com/monicahq/docker/tree/main/.examples#with-supervisor), we build our own image with the necessary scripts.

### Database

We are using the `mysql:5.7` image.

### Proxy

We used the `imori333/nginx-cloudflare-ssl-proxy` image (from [this repository](https://github.com/limtaegeun/Docker-nginx-cloudflare-ssl-proxy)), and configured Cloudflare for full SSL.

### Periodic Backups

We are running daily a simple script to backup the database to a folder in the host server. 
