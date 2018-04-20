### bgp-route-generator

Notes: You can edit the Dockerfile and pick a different dataset from RIPE if you like. I got mine from LONAP/LINX on this link: https://www.ripe.net/analyse/internet-measurements/routing-information-service-ris/ris-raw-data

1) import the image from docker hub
2) create a new machine
   `docker create -p 179:179/tcp -e "MYAS=65000" -e "PEERIP=192.168.99.232" -e "PEERAS=64599" fatred/bgp-route-generator:latest`
3) start the machine up
   `docker start <docker machine id>`
4) check the logs
   `docker logs <docker machine id>`