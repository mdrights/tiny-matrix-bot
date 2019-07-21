# CSObot Matrix Bot

- Forked from [tiny matrix bot](https://github.com/4nd3r/tiny-matrix-bot)
- This bot is part of [CSObot](https://github.com/mdrights/csobot), a bot trying to help Chinese civil society organisations.
- I am a simple [matrix](https://matrix.org) bot based on [matrix-python-sdk](https://github.com/matrix-org/matrix-python-sdk) with ~~no support~~ and no warranty.

## Functions
- ipfs-add: input a url of webpage then output several IPFS gateway links of that webpage.
- ipfs-id:	show the IPFS id of the bot.
- uptime:	show machine uptime.

- Alive on this Matrix room (for now): #csobot:matrix.org

## Change Log
- tiny-matrix-bot.py: modified as to parse and pass an argument to scripts.

## Quick Deployment
```
apt install python3 python3-requests curl jq
  (Also IPFS should be installed, default path: ~/go-ipfs/ipfs)
git clone https://github.com/mdrights/tiny-matrix-bot
git clone https://github.com/matrix-org/matrix-python-sdk
cd tiny-matrix-bot
ln -s ../matrix-python-sdk/matrix_client
cp tiny-matrix-bot.cfg.sample tiny-matrix-bot.cfg
vim tiny-matrix-bot.cfg
cp tiny-matrix-bot.service /etc/systemd/system
vim /etc/systemd/system/tiny-matrix-bot.service
systemctl enable tiny-matrix-bot
systemctl start tiny-matrix-bot
systemctl stop tiny-matrix-bot
```

Updated: 2019.07.21
