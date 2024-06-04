# instalation 
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest



# agent
docker run -d -p 9001:9001 --name portainer_agent --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v /var/lib/docker/volumes:/var/lib/docker/volumes portainer/agent:latest


# repositores templates

https://raw.githubusercontent.com/ntv-one/portainer/main/template.json

https://raw.githubusercontent.com/Qballjos/portainer_templates/master/Template/template.json


default:
https://raw.githubusercontent.com/portainer/templates/master/templates-2.0.json
