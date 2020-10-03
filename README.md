# build-v2ray-on-termux
```
pkg upgrade
pkg install golang wget
cd ~
wget https://github.com/v2fly/v2ray-core/archive/master.zip
unzip master.zip
cd ~/master
cd ~/master/main
env CGO_ENABLED=0 go build -o ~/v2ray/v2ray -ldflags "-s -w"

cd ~/master/infra/control/main
env CGO_ENABLED=0 go build -o ~/v2ray/v2ctl -tags confonly -ldflags "-s -w"
```
