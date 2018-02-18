# Synchronet Startup Scripts
Alternate startup scripts for the Synchronet BBS software - uses the "screen" command to manage session. This also restarts the BBS process if it crashes.

---
These start up the Synchronet BBS server at boot time with a "screen" process.

1. Copy synchronetbbs into /etc/init.d
2. Copy startsynchronetbbs into /sbbs
3. Run "**/etc/init.d/synchronetbbs start**"

When you want to view the SBBS console, just enter "**screen -r**" in your shell.

To disconnect from the SBBS console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /sbbs/nostart**". To reenable it type "**rm /sbbs/nostart**".