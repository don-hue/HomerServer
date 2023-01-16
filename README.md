# HomerServer - All-In-One Docker-Compose

## Introduction ##

Docker is a shining light in midst of environmental software-hell. As a curious brotege, I seeked enlightment. I set the sail of my old old ⛵, living like a pirate for decades. To hunt a 🐳, you have to think like a 🐳. So they say. A new era begins. Don-Hue rises.

The beauty of docker container is a hardware-agnostic attitude, which means that you can run a your container on every possible hardware as long as you have an x64/x86-cpu :rage4:. Even an old Mac mini from 2011 is a capable and cost-efficient solution. Due to Jellyfin, you can even stream your Media on every possible device that is connected to your local network. 

My current setup involves said Mac Mini 2011 (8GB ram, 60GB, intel i5, MacOS Mojave) and a FireTV for over a decade old tv. ***BTW this is just a fun project aka for learning purposes only.*** You should absolutely, definitely without any concern subscribe to every cloud-based streaming platform because buying merch and subscribe to endless streaming platforms is your life purpose, morty. And you did it. You didn't ask too much questions, just tickle those monthly payments, morty :feelsgood:. 

P.S. I choosed a Mac Mini because I love the fact that I cannot upgrade the storage. I forces me to write better code :godmode:.

## Short Overview ##
I am a copycat 🐈, I mean developer :shipit:

### Trassmisison - https://github.com/haugene/docker-transmission-openvpn ###
Transmission is a light-weight download-client. In this configuration, you can incorporate your VPN account, so that transmission dowload via a VPN connection. 

### Jackett - https://github.com/Jackett/Jackett###
Jackett works as a proxy server: it translates queries from apps (Sonarr, Radarr, SickRage, CouchPotato, Mylar3, Lidarr, DuckieTV, qBittorrent, Nefarious etc.) into tracker-site-specific http queries, parses the html or json response, and then sends results back to the requesting software. 

We will need Jackett for indexer configuration within Sonarr and Radarr.

### Sonarr (for TV-Shows) and Radarr (for Movies) - https://github.com/linuxserver/docker-sonarr & https://github.com/linuxserver/docker-radarr ###
You will follow the same configuration steps.
Once the container is running, just go the localhost:Port (sometimes, you will need to enter the acutal IP-adress e.g. 194.135.0.23:PORT) Your local IP is individual. You can get the IP-adress via command line. (ifconfig on MacOS)

1) Settings -> Download-Client
2) Add Transmission (tipp: Use your IP-adress as url)
3) Settings -> Indexer -> Tornznab
4) Copy URL from Jackett and paste it to Sonarr/Radarr
5) Copy API-Key from Jackett

Pro Tipp: Setting -> Media Management -> enable: create subfolder for Series. 
-> Sonarr will create a subfolder and organize your TV series by Name. 

### Jellyfin - Your Media Streamer ###
I prefer Jellyfin over Kodi as Jellyfin is built for streaming whereas Kodi is not. 

Jellyfin is actually pretty easy peazy to setup. Just follow the instructions. 

Pro tipp: You don't have to use a password. And honestly, it is easier. But if you like to Edward Snowden your own local network, I guess feel free to set a password that you will forget within the moment you made it. 
 gg :rage4:

Once Jellyfin is running on your Homeserver, you can basically connect any device that you want to watch your media on via the localhost:8086 e.g. A fireTV stick. 

### Jellyseer - The Overlord is watching ###
Now, go full sunglasses fabio look, smirk like you know something others don't and buckle up those ass cheeekss :godmode:

If Jellyfin is the bread and butter, Jellyseer is the topping. 

Jellyseer basically is a proxy-server that puts forward your search request to Sonarr and Radarr combined with a super nice UI that acutally gives you information and recommendations. Noise 🪗

## Paths - Get your head arround it :shipit: ##
If you are new to docker and container, there are some things you need to know. 

1) every container needs persmissions. 
2) there are directory path on YOUR machine and directory path WIHTIN the container. 
