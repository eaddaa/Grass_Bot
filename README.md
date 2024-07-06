# Grass_Bot
# GetGrass Bot Setup Instructions

## Server Requirements
- **RAM:** 8GB
- **OS:** Ubuntu

## Proxy Requirements
- **Type:** Residential Static Proxy
- **Protocol:** Socks5
- **Proxy Format:** `socks5://username:password@IP:Port`
- **Note:** ParentHost removed due to slow order processing

## Getting UserID
1. Open Grass Dashboard.
2. Press `F12` to open the console.
3. Enter the following command to get UserID:
```
   localStorage.userId
```
Running the Bot
Connect to your server.
Run the following commands:
```
sudo apt update && \
sudo apt install python3-pip -y && \
pip3 install websockets_proxy loguru && \
git clone https://github.com/ymmmmmmmm/getgrass_bot.git && \
cd getgrass_bot && \
nano main.py
```
Find _user_id and socks5_proxy_list in main.py.
Replace them with your UserID and Proxy. To add multiple proxies, separate them with a comma (,).
After editing, press CTRL+X, then Y, and Enter.
Run the following commands to start the bot:
```
screen -R grass && \
cd getgrass_bot && \
python3 main.py
```
That's it! The bot will start running. You can close the terminal as it's running in a screen session.

use socks5 try 443 port 
if didnt work unset proxy and try another one
```
unset http_proxy
unset https_proxy

```

set socks5

```
export http_proxy=socks5://199.102.105.242:443
```
and then test it

```
curl -I https://www.google.com
curl -I http://www.google.com
```



