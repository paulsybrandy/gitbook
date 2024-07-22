# Portainer on Windows

Using a powershell prompt (non-administrator) type the following:

`docker run -d -p 9000:9000 -v portainer_data:/data portainer/portainer-ce -H tcp://10.0.75.1:2375`

_**Portainer will be available at**_ [_**http://localhost:9000**_](http://localhost:9000)

***

To run Portainer container in a native Windows container, the syntax is:

```
docker run -d -p 9000:9000 --name portainer --restart always -v \\.\pipe\docker_engine:\\.\pipe\docker_engine -v C:\ProgramData\Portainer:C:\data portainer/portainer-ce
```

For more info, check [this link](https://portainer.readthedocs.io/en/latest/deployment.html).
