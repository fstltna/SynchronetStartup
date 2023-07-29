# Synchronet Startup Scripts (1.8.1)
Alternate startup scripts for the Synchronet BBS software - uses the "screen" command to manage session. This also restarts the BBS process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/SynchronetStartup) - [Official Forum](https://synchronetbbs.org/index.php/forum/alternate-startup-scripts) 
![Synchronet Logo](https://SynchronetBBS.org/SynchronetLogo.png) 

[![Visit our IRC channel](https://kiwiirc.com/buttons/irc.synchro.net/SynchronetFans.png)](https://kiwiirc.com/client/irc.synchro.net/?nick=guest|?#SynchronetFans)

---
These start up the Synchronet BBS server at boot time with a "screen" process.

1. Copy **synchronetbbs** into **/etc/init.d** - make sure it is executable
2. Copy **startsynchronetbbs** into **/sbbs** - make sure it is executable
3. Run "**systemctl enable synchronetbbs**" (only needed once, will stick)
4. Run "**systemctl start synchronetbbs**" - starts sbbs without restarting the server
5. Run **./Update_Script** if you need to update the watchdog

When you want to view the SBBS console, just enter "**screen -r**" in your shell.

To disconnect from the SBBS console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

If you want to turn off the server respawning type "**touch /sbbs/nostart**". To reenable it type "**rm /sbbs/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
