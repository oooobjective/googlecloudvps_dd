# googlecloudvps_dd

#获取root权限
```
sudo -i
```
#获取系统更新及安装wegt sudo
```
apt update -y && apt install -y wget sudo
```
#dd系统脚本

内网网关为内网地址最后一位为.1

d 11: debian 11系统

p 123456：密码

port 22：端口
```
bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/MoeClub/Note/master/InstallNET.sh') --ip-addr 谷歌云内网地址 --ip-gate 内网网关 --ip-mask 255.255.255.0 -d 11 -v 64 -p 123456 -port 22
```

#ssh工具进系统后改密码
```
passwd
```
#系统更新
```
apt update -y && apt full-upgrade -y && apt install -y curl wget sudo socat
```
#vps cpu性能测试（单核多核）
```
curl -sL yabs.sh | bash -s -- -i -5
```
#三网回程测试
```
curl https://raw.githubusercontent.com/zhucaidan/mtr_trace/main/mtr_trace.sh|bash
```
#三网回程延迟测试
```
wget -qO- git.io/besttrace | bash
```
#vps网络测速
```
wget -qO- bench.sh | bash
```
