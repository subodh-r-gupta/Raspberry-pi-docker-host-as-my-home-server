# My homelab on Raspberry pi 4
my notes of creating a homelab on raspberry pi
---

So I got a new raspberry pi 4 and I wanted to build a low cost and low power consuming home server on it. 

## Which services do I want to run on it?

I need a home server which can provide the following services-

### Security Services

| Service | Description |
| ----------- | ----------- |
| pivpn | for accessing services over internet when i am travelling with my laptop  |
| cloudflare ddns | for providing me a dynamic dns server to connect my vpn clients to  |


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

Yes, I know the for server management a CLI must be used but sometimes a GUI is good to cheat through.

### Entertainment Services
| Service | Description |
| ----------- | ----------- |
| jellyfin |  for sharing music and videos to my laptop and tv  |
| minidlna |  for sharing music and videos to my laptop and tv  |

In my previous tests on raspberry pi, jellyfin was maxing out CPU usage, So i will have a lighweight alternative as minidlna on docker host to fall back if it happens again.

### File Sharing Services

| Service | Description |
| ----------- | ----------- |
| samba |  for sharing files within the LAN  |

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







