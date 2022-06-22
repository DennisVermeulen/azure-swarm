traeffik

traefik.enable true
traefik.http.routers.iis.entrypoints websecure
traefik.http.routers.iis.rule Host(`denver-rumewfkk.westeurope.cloudapp.azure.com`) && PathPrefix(`/hello`)
traefik.http.routers.iis.tls.certresolver myresolver
traefik.http.services.iis.loadBalancer.server.port 80
traefik.http.services.iis.loadBalancer.server.scheme http