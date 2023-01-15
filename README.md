# HomerServer - All-In-One Docker-Compose

## Introduction ##

Docker is a shining light in midst of environmental software-hell. As a curious brotege, I seeked enlightment. I set the sail of my old old ⛵, living like a pirate for decades. To hunt a 🐳, you have to think like a 🐳. So they say. A new era begins. Don-Hue rises.

The beauty of docker container is a hardware-agnostic attitude, which means that you can run a your container on every possible hardware as long as you have an x64/x86-cpu :rage4:. Even an old Mac mini from 2011 is a capable and cost-efficient solution. Due to Jellyfin, you can even stream your Media on every possible device that is connected to your local network. 

My current setup involves said Mac Mini 2011 (8GB ram, 60GB, intel i5, MacOS Mojave) and a FireTV for over a decade old tv. BTW this is just a fun project aka for learning purposes only. You should absolutely, definitely without any concern subscribe to every cloud-based streaming platform because buying merch and subscribe to endless streaming platforms is your life purpose, morty. And you did it. You dinn't ask too much questions, just tickle those monthly payments, morty :feelsgood:. 

P.S. I choosed a Mac Mini because I love the fact that I cannot upgrade the storage. I forces me to write better code :godmode:.

## Short Overview ##
I am a copycat 🐈, I mean developer :shipit:

### Trassmisison ###
Transmission is a light-weight download-client. In this configuration, you can incorporate your VPN account, so that transmission dowload via a VPN connection. https://github.com/haugene/docker-transmission-openvpn

### Jackett ###
Jackett works as a proxy server: it translates queries from apps (Sonarr, Radarr, SickRage, CouchPotato, Mylar3, Lidarr, DuckieTV, qBittorrent, Nefarious etc.) into tracker-site-specific http queries, parses the html or json response, and then sends results back to the requesting software. https://github.com/Jackett/Jackett

We will need Jackett for indexer configuration within Sonarr and Radarr.

### Sonarr (for TV-Shows) and Radarr (for Movies) ###
Sonarr
