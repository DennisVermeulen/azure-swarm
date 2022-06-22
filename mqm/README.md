MQM SWARM TRAFFIC SETTINGS

com.docker.stack.image mqm
com.docker.stack.namespace base
traefik.enable true
traefik.http.middlewares.limit.buffering.maxRequestBodyBytes 500000000
traefik.http.routers.mqm.entrypoints websecure
traefik.http.routers.mqm.rule Host(`denver-wkdqpdug.westeurope.cloudapp.azure.com`) && PathPrefix(`/`)
traefik.http.routers.mqm.tls.certresolver myresolver
traefik.http.services.mqm.loadBalancer.server.port 8161
traefik.http.services.mqm.loadBalancer.server.scheme http
traefik.http.middlewares.mqm.stripprefix.prefixes /mqm
traefik.http.routers.mqm.service mqm@docker
admin admin