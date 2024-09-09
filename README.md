# nextcloud-docker-cloudflare
Nextcloud Docker Deployment for Cloudflare


```
sudo docker run \
--init \
--sig-proxy=false \
--name nextcloud-aio-mastercontainer \
--restart always \
--publish 8080:8080 \
--env APACHE_PORT=11000 \
--env APACHE_IP_BINDING=0.0.0.0 \
--env SKIP_DOMAIN_VALIDATION=true \
--volume nextcloud_aio_mastercontainer:/mnt/docker-aio-config \
--volume /var/run/docker.sock:/var/run/docker.sock:ro \
nextcloud/all-in-one:latest
```



References:  
https://github.com/nextcloud/all-in-one#how-to-skip-the-domain-validation  
https://github.com/nextcloud/all-in-one/blob/main/reverse-proxy.md
