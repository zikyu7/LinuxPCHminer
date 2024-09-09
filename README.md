# LinuxPCHminer
For linux pc.

# STBminev

# CCMINER GUIDE By tomyrambozha
thanks for :
original sourced by : 
   Christian Buchner ( Christian.Buchner@gmail.com )
   Christian H. ( Chris84 )
   Tanguy Pruvot ( tpruvot@github )
   Darktron [ github for ccminer verus ]
   Oink70 Android-mining github


## [ install update ] 
```
apt-get update
```

## [ install libs]
```
apt-get install git

```

## [ Clone Repo]
```
git clone https://github.com/zikyu7/linuxPCHminer
mv linuxPCHminer Hminer
cd Hminer
chmod +x Hminer start.sh
```

## Edit config Json to your wallet and worker name, and --cpu from 4-48 for pc (core /thread)
```
nano start.sh
```

## RUN MINER TEST: 
```
bash start.sh
```
## IF YOU WANT SCRIPT RUN AUTOMATICALLY AFTER REBOOT
use this option

( first stop ccminer :
ctrl + C on keyboard )

[ OPTION 1 ] CRONTAB [ RECOMENDED ] 

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
./hellminer -c stratum+tcp://sg.vipor.net:5040 -u RV3mdCWXgijaKCvpu764Xm9zmHzGRY6jjG.XE5 -p x --cpu 48


type : 

``` 
cd ..
crontab -e
``` 
type this shell command on first line : 
```
@reboot bash /root/start.sh >> /root/miner.log 2>&1

```
screen will not show mining progress but you can see log by type : 

```
 cat /root/ccminer/miner.log
```
just repeat if you want to see more 
