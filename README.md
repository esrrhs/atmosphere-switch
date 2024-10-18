# atmosphere-switch
大气层switch破解方案

# 准备
* 可以软破的switch
* RCM注入器v5，某宝上有售
* sd卡，格式化为fat32

# 准备SD卡
* 下载[大气层](https://github.com/Atmosphere-NX/Atmosphere)最新版
* 把atmosphere-xxxxxx-master-xxxxxxxx+hbl-xxx+hbmenu-xxx.zip解压到sd卡
* 下载fusee.bin，下面会用到
* 下载[hekate](https://github.com/CTCaer/hekate)最新版
* 把 hekate_ctcaer_xxxx_Nyx_xxx.zip解压到sd卡
* 留意这里的hekate_ctcaer_xxx.bin，下面会用到
* 把RCM注入器插入电脑，会识别为U盘
* 打开\ATMOSPHERE_HEKATE，把刚才的hekate_ctcaer_xxx.bin复制为payload.bin，然后拔掉
* 把刚才的fusee.bin拷贝到switch的sd卡，放到bootloader\payloads目录
* 把[hekate_ipl.ini](./hekate_ipl.ini)拷贝到sd/bootloader/目录
* 下载[patches](https://gbatemp.net/threads/sigpatches-for-atmosphere-hekate-fss0-fusee-package3.571543/)最新版
* 把sigpatches.zip解压到switch的sd卡
* （可选）下载安装工具[tinfoil](https://tinfoil.io/)的最新NRO版本，解压tinfoil.latest.zip到switch的sd卡
* （可选）下载安装工具[DBI](https://github.com/rashevskyv/dbi)的dbi.nro、dbi.config，放入switch/DBI/目录
* （可选）下载安装工具[Awoo-Installer](https://github.com/Huntereb/Awoo-Installer)，下载解压到sd卡
* （可选）下载叠加层加载工具[nx-ovlloader](https://github.com/WerWolv/nx-ovlloader)，下载解压到sd卡。下载叠加层[Tesla-Menu](https://github.com/WerWolv/Tesla-Menu)
* （可选）下载存档修改工具[EdiZon](https://github.com/WerWolv/EdiZon)的Edizon.nro，放入switch目录下。下载ovlEdiZon.ovl放到switch\.overlays目录

# 启动
* 按住开关10秒，把switch强行关机
* 插入短接器，同时按音量+、电源键，然后放开
* 长按RCM注入器的加号，直到闪烁蓝灯，说明是大气层模式。不是则放开，再长按切换
* RCM注入器插入到switch
* switch启动到boot界面

# 备份系统
* 点击tools

![image](backup1.png)

* 点击backup emmc

![image](backup2.png)

* 点击第一个

![image](backup3.png)

* 结束关闭

![image](backup4.png)

* 点击第二个

![image](backup5.png)

* 结束关闭

![image](backup6.png)

* 最终的backup目录，可以拷贝到其他地方保存

![image](backup7.png)

# 虚拟系统
https://switch.homebrew.guide/emummc/emummc.html

# 安装游戏
* 安装[Awoo-Installer](https://github.com/Huntereb/Awoo-Installer)，下载解压到sd卡
* 按住R，打开任意一个游戏，出现app界面，选择Awoo，或者直接从相册进入打开Awoo
* 进入后，选择usb安装
* 在电脑上下载[ns-usbloader](https://github.com/developersu/ns-usbloader)，拖入游戏，点击上传
* Awoo里选择游戏，安装即可

