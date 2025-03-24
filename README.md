# Hexactyl
Hexactyl is an open-source dashboard for pterodactyl based on Heliactyl's legacy. Hexactyl is the official successor of Ethan James's Lexactyl/Spaceport

# Features
- Resource Management (Use it to create servers, gift them, etc)
- Coins (AFK Page earning, Linkvertise earning, Gift them away)
- Coupons (Gives resources & coins to a user)
- Servers (create, view, edit servers)
- User System (auth, regen password, etc)
- Store (buy resources with coins)
- Dashboard (view resources)
- Join for Rewards (join discord servers for coins)
- Admin (set/add/remove coins & resources, create/revoke coupons)
- API (for bots & other things)

# What happened to V1.x (Lexactyl/Spaceport)
Due to major issues with the version, we've decided to come back to v12 and recontinue it
The latest versions will be on v12 now

# Warning
Using cloudflare proxy can disable anti-alt and VPN Check

# Installation
1. Download the code ``git clone https://github.com/hashirsucksatdev/hexactyl/``
2. Install nodejs
3. ``cd hexactyl`` and ``npm install``
4. Rename config-example.toml to config.to

# Updating 

From Heliactyl v12 or Dashactyl v0.4 to Hexactyl v12:
1. Store certain things such as your api keys, discord auth settings, etc in a .txt file
2. Download database file and rename it with hexactyl3.sqlite
3. Delete all files off the server (or delete and remake the folder if done in ssh)
4. Upload the latest Hexactyl v12 release and unzip it
5. Upload database file and reconfigure config.tomel

From Lexactyl v1.x:
- This is currently not possible due to major differences between the versions


# Running in background / on startup, on a server instead of within Pterodactyl

Installing [pm2](https://github.com/Unitech/pm2):
- Run `npm install pm2 -g` on the server

Starting the Dashboard in Background:
- Change directory to your Hexactyl folder Using `cd` command, Example: `cd /var/www/hexactyl` 
- To run Heliactyl, use `pm2 start index.js --name "hexactyl"`
- To view logs, run `pm2 logs Hexactyl`

Making the dashboard runs on startup:
- Make sure your dashboard is running in the background with the help of [pm2](https://github.com/Unitech/pm2)
- You can check if Hexactyl is running in background with `pm2 list`
- Once you confirmed that Hexactyl is running in background, you can create a startup script by running `pm2 startup` and `pm2 save`
- Note: Supported init systems are `systemd`, `upstart`, `launchd`, `rc.d`
- To stop your Hexactyl from running in the background, use `pm2 unstartup`

To stop a currently running Hexactyl instance, use `pm2 stop hexactyl`

# Legacy Deprecation Notice

Falcon (EOL), Lexactyl/Spaceport is now deprecated as listed in our github and should not be used.
Please update to Hexactyl v12.

# Contribution
Feel free to contribute.
