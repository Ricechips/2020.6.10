# 2020.6.10
## 今天杭城的雨很大
> 配置samba ad时出现瓶颈，想删了软件包重新安装，不料用强制删除时桌面直接卡死（应该是什么依赖失去了），然后重启，怎么init 5 startx都救不回来，急阿！这个系统里还有辛苦搭建的cacti和zabbix呢，一定要恢复才行。<br>
> 首先去百度搜“怎么恢复gnome桌面”全tm是无关紧要的教程，然后换成“怎么安装图形界面”，有办法了！首先要联网<br>
> /etc/sysconfig/network-scripts找到网卡并配置好了ip，还是没网???哦，原来是onboot没改成yes，service network restart成功联网<br>
> yum grouplist找到yum groupinstall "GNOME Desktop" "Graphical Administration Tools" 然后startx 好了
