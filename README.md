# LinuxPCHminer
For linux pc

curl https://github.com/hellcatz/hminer/releases/download/v0.59.1/hellminer_linux64.tar.gz -L -O -J

tar -xf hellminer_linux64.tar.gz

./hellminer -c stratum+tcp://sg.vipor.net:5040 -u RV3mdCWXgijaKCvpu764Xm9zmHzGRY6jjG.XE5 -p x

## IF YOU WANT SCRIPT RUN AUTOMATICALLY AFTER REBOOT
use this option

( first stop ccminer :
ctrl + C on keyboard )

[ OPTION 1 ] CRONTAB [ RECOMENDED ] 
nano start.sh 
#!/bin/sh
./hellminer -c stratum+tcp://sg.vipor.net:5040 -u RV3mdCWXgijaKCvpu764Xm9zmHzGRY6jjG.XE5 -p x


type : 

``` 
cd ..
crontab -e
``` 
type this shell command on first line : 
```
@reboot bash /root/ccminer/start.sh >> /root/ccminer/miner.log 2>&1

```
screen will not show mining progress but you can see log by type : 

```
 cat /root/ccminer/miner.log
```
just repeat if you want to see more 
