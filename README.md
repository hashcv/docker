# docker

docker build nexus3
docker run -d -p 8081:8081 -p 8443:8443 -p 18443:18443 container_id

Access to admin interface - https://server_ip:8443
Username admin
Password admin123

vi /etc/sysconfig/docker
INSECURE_REGISTRY='--insecure-registry 127.0.0.1:18443'

docker login 127.0.0.1:18443
admin
admin123

docker tag container_id 127.0.0.1:18443/nexus3
docker push 127.0.0.1:18443

