# My homelab on Raspberry pi 4


So I got a new raspberry pi 4 and I want to build a low cost and low power consuming home server on it. Here we go again...

## Which services do I want to run on it?

I need a home server which can provide the following services-

### Security Services

| Service | Description |
| ----------- | ----------- |
| pivpn | for accessing services over internet when i am travelling with my laptop  |
| cloudflare ddns | for providing me a dynamic dns server to connect my vpn clients to  |
| duckdns| for providing me a dynamic dns server to connect my vpn clients to  |
| linux firewall | for blocking intrusions  |
| nginx proxy manager | all containers will be placed behind a proxy to reduce attack surface |
| traefik | all containers will be placed behind a proxy to reduce attack surface |

My previous experience with traefik was not good, the documentation was a mess to figure out, so this time i am going to have nginx proxy manager and traefik both. I will test and choose one.

Similarly i have used duckdns in past, it worked well for me. But i have heard good things about cloudfare so I would like to try both of them and then decide on one of them.

### Privacy Services

| Service | Description |
| ----------- | ----------- |
| pihole |  for Network-Wide Ad Blocking  |
| adguard |  for Network-Wide Ad Blocking  |

I am going to have pihole and adguard both for side by side comparison. I have been using pihole for years, but heard good things about adguards. So why not have then both and test which one works better for me?



### Server Management Services

| Service | Description |
| ----------- | ----------- |
| dashy |  for a nice looking server home page with links to all the services  |
| cockpit |  for a nice server manager gui  |
| portainer | for easy docker container management using web gui |

Yes, I know the for server management a CLI must be used but sometimes a GUI is good to cheat through.

### Server Monitoring and Alert services

| Service | Description |
| ----------- | ----------- |
| netdata |  for server and network monitoring and alerts  |
| zabbix |  for server and network monitoring and alerts  |
| glances | for a quick view of docker container health |
| Librenms | for server and network monitoring alerts

This server needs to be monitored 24x7 and i should be able to get alerts when something fails or an attack happens. I would like to compare netdata, zabbix and librenms, so I will configure them all.Once i choose one over other, It will be cleaned up.


### Entertainment Services
| Service | Description |
| ----------- | ----------- |
| jellyfin |  for sharing music and video library to my laptop and tv  |
| minidlna |  for sharing music and video library to my laptop and tv  |
| calibre and calibre web |  for sharing comics and books library to my laptop and tv  |
| photoprism | for sharing photos to my laptop and tv |


In my previous tests on raspberry pi, jellyfin was maxing out CPU usage, So i will have a lighweight alternative as minidlna on docker host to fall back if it happens again.

### File Sharing Services

| Service | Description |
| ----------- | ----------- |
| samba |  for storing and sharing important personal documents within the LAN  |

I have a spare 500 GB HDD which I will use as network attached storage for storing all my data.

### Office Services
| Service | Description |
| ----------- | ----------- |
| nextcloud |  for office apps, document sharing and meetings with friends and family over the internet |

### Website hosting services

| Service | Description |
| ----------- | ----------- |
| wordpress |  for selfhosting my own website |

I am a cheapskate, I do not want to pay for hosting charges every year.

----

# Getting Started...

## 1 - Inventory -

- Raspberry Pi 4B 8 gb
- Micro SD Card
- Heat Sink
- Power Supply
- Rpi4 Case With Fan
- Micro HDMI to HDMI cable
- External HDD

## 2 - Installing Ubuntu Server 2204 LTS on raspberry pi 4

I am using Ubuntu and Red Hat Linux at work on daily basis. 

But I have decided to choose Ubuntu server 2204 LTS as the base OS for this server because...

- they have the official LTS builds available for RPI
- ease of use.
- no money to buy support

This will be my docker host.


## 3 - Installing docker


### - Setting up services




