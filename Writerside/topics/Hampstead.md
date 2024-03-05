# Hampstead
Hampstead is the non-critical, but useful to have server.
## Steam Cache
The steam cache utilizes LanCache from https://lancache.net/, it caches Steam, BattleNet, and Epic Games downloads.

Instead of downloading a game from the internet over and over, if it is cached, it simply pretends to be Steam and provides the download files itself. This saves time, and network bandwidth.
## Uptime
The uptime monitor runs UptimeKuma, a docker based monitoring system. It sends messages to room admins when services die, and provides a webview at http://192.168.30.12:3001/status/main.
## Webserver
NGINX is configured to host https://professoreno.com on Port 81. https://docs.professoreno.com is hosted on pot 82. These are tunneled through cloudflare to provide access outside of the local network.
## Network Share
A public network share is hosted here, holding ISOs and the Golden Drive Image,