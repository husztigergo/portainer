##### Note, that when you want to use NGINX Proxy Manager with Portainer, you need to put both containers in the same network, and don't expose the admin port 9000.
```sh
docker run -d -p 8000:8000 --network nginxproxymanager_default --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
```
