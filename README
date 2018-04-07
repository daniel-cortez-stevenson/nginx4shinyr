# nginx4shinyr

### Usage
1. Set upstream host name in nginx.conf to the hostname of the docker service running shiny-server (default is 'shiny').
* You also may need to change the port, on which shiny is exposed (default is '3838').
* Make sure the shiny Docker service is connected to a Docker network, note the name of the network.
* Set username and password hash in .htpasswd file (or you can use the defaults, I guess)
* run<pre>
docker run -v "`pwd`/.htpasswd":/etc/nginx/.htpasswd \
        -name nginx \
        -p 80:8080 \
        --network=shiny_network_name \
        danielstevenson/nginx4shinyr:latest
</pre>
* Find your shiny app at http://localhost:80
