# [[281677160/build-openwrt的专用软件包](https://github.com/281677160/build-openwrt.git)]

#
#### 分支[master]的为lede源码专用，分支[19.07]的为lienol源码专用，分支[project-18.06]的为project源码专用
#

##### 添加以下插件
###### luci-theme-rosy    &nbsp;&nbsp;&nbsp;&nbsp;#主题-rosy
###### luci-theme-edge    &nbsp;&nbsp;&nbsp;&nbsp;#主题-edge
###### luci-theme-opentomcat   &nbsp;&nbsp;&nbsp;&nbsp;#主题-opentomcat
###### luci-theme-opentopd   &nbsp;&nbsp;&nbsp;&nbsp;#主题-opentopd<br>
###### luci-theme-atmaterial   &nbsp;&nbsp;&nbsp;&nbsp;#atmaterial-主题<br>
###### luci-theme-rosy   &nbsp;&nbsp;&nbsp;&nbsp;#主题-rosy<br>
###### luci-theme-infinityfreedom    &nbsp;&nbsp;&nbsp;&nbsp;#透明主题<br>
###### luci-app-openclash    &nbsp;&nbsp;&nbsp;&nbsp;#openclash 出国软件<br>
###### luci-app-clash    &nbsp;&nbsp;&nbsp;&nbsp;#clash 出国软件<br>
###### luci-app-serverchan    &nbsp;&nbsp;&nbsp;&nbsp;#微信推送<br>
###### luci-app-eqos    &nbsp;&nbsp;&nbsp;&nbsp;#内网控速 内网IP限速工具<br>
###### luci-app-jd-dailybonus    &nbsp;&nbsp;&nbsp;&nbsp;#京东签到<br>
###### luci-app-passwall    &nbsp;&nbsp;&nbsp;&nbsp;#passwall 出国软件<br>
###### luci-app-advanced    &nbsp;&nbsp;&nbsp;&nbsp;#高级设置<br>
###### luci-app-poweroff    &nbsp;&nbsp;&nbsp;&nbsp;#关机（增加关机功能）<br>
###### luci-theme-argon    &nbsp;&nbsp;&nbsp;&nbsp;#新的argon主题<br>
###### luci-app-argon-config    &nbsp;&nbsp;&nbsp;&nbsp;#argon主题设置（编译时候选上,在固件的‘系统’里面）<br>
###### luci-app-k3screenctrl   &nbsp;&nbsp;&nbsp;&nbsp;#k3屏幕，k3路由器专用<br>
###### luci-app-koolproxyR   &nbsp;&nbsp;&nbsp;&nbsp;#广告过滤大师 plus+  ，慎用，不懂的话，打开就没网络了<br>
###### luci-app-oaf （OpenAppFilter）  &nbsp;&nbsp;&nbsp;&nbsp;#应用过滤 ，该模块只工作在路由模式， 旁路模式、桥模式不生效，还有和Turbo ACC 网络加速有冲突<br>
###### luci-app-ssr-plus   &nbsp;&nbsp;&nbsp;&nbsp;#shadowsocksR Puls+  出国软件<br>
###### luci-app-vssr   &nbsp;&nbsp;&nbsp;&nbsp;#Hello World 也叫彩旗飘飘  出国软件<br>
###### luci-app-gost   &nbsp;&nbsp;&nbsp;&nbsp;#GO语言实现的安全隧道<br>
###### luci-app-cpulimit   &nbsp;&nbsp;&nbsp;&nbsp;#CPU性能限制<br>
###### luci-app-wrtbwmon-zhcn   &nbsp;&nbsp;&nbsp;&nbsp;#流量统计，替代luci-app-wrtbwmon，在固件状态栏显示<br>
###### luci-app-autopoweroff   &nbsp;&nbsp;&nbsp;&nbsp;#定时自动关机，替代luci-app-autoreboot<br>
###### luci-app-control-webrestriction   &nbsp;&nbsp;&nbsp;&nbsp;#访问限制<br>
###### luci-app-control-weburl   &nbsp;&nbsp;&nbsp;&nbsp;#网址过滤<br>
###### luci-app-modeminfo    &nbsp;&nbsp;&nbsp;&nbsp;#OpenWrt LuCi的3G / LTE加密狗信息<br>
###### luci-app-filebrowser   &nbsp;&nbsp;&nbsp;&nbsp;#文件浏览器<br>
###### luci-app-gowebdav   &nbsp;&nbsp;&nbsp;&nbsp;#GoWebDav 是一个轻巧、简单、快速的 WebDav 服务端程序<br>
###### luci-app-smartinfo   &nbsp;&nbsp;&nbsp;&nbsp;#磁盘监控 ，该工具帮助您通过S.M.A.R.T技术来监控您硬盘的健康状况<br>
###### luci-app-pptp-vpnserver-manyusers   &nbsp;&nbsp;&nbsp;&nbsp;#PPTP VPN 服务器
###### luci-app-smartdns   &nbsp;&nbsp;&nbsp;&nbsp;#smartdns DNS加速<br>
###### luci-app-adguardhome   &nbsp;&nbsp;&nbsp;&nbsp;#adguardhome<br>
###### luci-app-dockerman   &nbsp;&nbsp;&nbsp;&nbsp;#docker容器，和源码自带的luci-app-docker不能同时编译，同时编译会失败，所以要注意<br>

#

- luci-app-advanced 和 luci-app-filebrowser 不能同时编译，同时编译会失败
- luci-app-samba 和 luci-app-samba4 不能同时编译，同时编译会失败
- 想选择luci-app-samba4，首先在Extra packages ---> 把autosamba取消，然后在Network ---> 把 samba36-server取消，最后选择luci-app-samba4，记得顺序别搞错
- luci-app-dockerman 和 luci-app-docker 不能同时编译，同时编译会失败

#
##### N1盒子写入emmc方法
- 1、SSH连接配置固件时候找到 Utilities 里面的 install-program  按键盘的y选择上，插件里面也选上luci-app-ttyd方便后续执行命令
- 2、编译完成之后使用【balenaEtcher】把镜像写入U盘在盒子上启动，之后用固件里的ttyd（命令窗）或者SSH执行 n1-install 命令，即可安装到 emmc
- 3、这是我根据作者描述个人理解为这样的，我没N1盒子没办法测试，有谁测试过的什么情况请告知
#
#
##### 如果还是没有你需要的插件，请不要一下子就拉取别人的插件包
##### 相同的文件都拉一起，因为有一些可能还是其他大神修改过的容易造成编译错误的
##### 想要什么插件就单独的拉取什么插件就好，或者告诉我，我把插件放我的插件包就行了
#
#
## 感谢各位大神的源码，openwrt有各位大神而精彩，感谢！感谢！，插件每天白天12点跟晚上12点都同步一次各位大神的源码！

#

# 请不要Fork此仓库，你Fork后，插件不会自动根据作者更新而更新!!!!!!!!!!!
