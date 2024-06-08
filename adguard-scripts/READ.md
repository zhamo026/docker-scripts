# AdguardSync: 
[Source-bakito](https://github.com/bakito/adguardhome-sync)


```bash
---
version: "2.1"
services:
  adguardhome-sync:
    image: quay.io/bakito/adguardhome-sync
    container_name: adguardhome-sync
    command: run
    environment:
      - ORIGIN_URL=http://192.168.x.x #IP and/or port as necessary 
      - ORIGIN_USERNAME=user #add user
      - ORIGIN_PASSWORD=password #add password
      - REPLICA_URL=http://192.168.x.x #IP and/or port as necessary 
      - REPLICA_USERNAME=user #add user
      - REPLICA_PASSWORD=password #add password
      #addmore instances if necessary
      - CRON=*/1 * * * * # run every 1 minute
      - RUNONSTART=true
    ports:
      - 8080:8080 #change as necessary
    restart: unless-stopped    

``` 
