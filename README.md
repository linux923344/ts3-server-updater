# TeamSpeak3 - Updater 

I use teamspeak server as a service. If you want to have the same setting (i.e when you want stop your teamspeak server you can write:
```
systemctl stop teamspeak
```

If you have not got it. You can easly copy like this:
```
git clone https://github.com/linux923344/ts3-server-updater.git
cd ts3-server-updater
sudo cp teamspeak.service /usr/lib/systemd/system/
sudo systemctl daemon-reload
```
## Instalation teamspeak.service
In the file **teamspeak.service** the default localization is **/opt/teamspeak/** and the default user is **teamspeak**. You can change it for your settings of course. Also in the when you have different localization you **MUST** change it in the ```update``` in the variable ``ts3local``.

Now you have ```systemctl``` for stop or start your service.
 

## Updating...
If you did not commit my repo, you should do it now.
```
git clone https://github.com/linux923344/ts3-server-updater.git
cd ts3-server-updater
```
When you want to run your updater. Check remove in variable link in the file update to newer version. You can check it on the website: https://www.teamspeak.com/en/downloads/#server

```
./update
```

The update will be do a backup. The file ``backup-remove`` and ``backup`` I use it for cron ``crontab -e`` !


```
#BACKUP EVERYDAY AT 5AM
0 5 * * *	/opt/backup

#BACKUP EVERY SUNDAY AT 6AM AND ALSO STAY 2 OF THEM
0 6 * * SUN     /opt/backup-remove

```

If You wanna contact with me write to me on private message or write to y0rune@aol.com
