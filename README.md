# atmosphere-switch
大气层switch破解方案

# 准备
* 可以软破的switch
* RCM注入器v5，某宝上有售
* sd卡

# 准备SD卡
* 下载[大气层](https://github.com/Atmosphere-NX/Atmosphere)最新版
* 解压到sd卡
* 下载[hekate](https://github.com/CTCaer/hekate)最新版
* 解压到sd卡
* 留意这里的hekate_ctcaer_xxx.bin，插入RCM注入器到电脑
* 会识别为U盘，打开\ATMOSPHERE_HEKATE，把刚才的hekate_ctcaer_xxx.bin复制为payload.bin，然后拔掉
* 插入sd卡到switch

# 启动
* 按住开关10秒，把switch强行关机
* 插入短接器，同时按音量+、电源键，然后放开
* 长按RCM注入器的加号，直到闪烁蓝灯，说明是大气层模式。不是则放开，再长按切换
* RCM注入器插入到switch
* switch启动到boot界面

# 安装补丁
* 打开网站[sdsetup](https://www.sdsetup.com/)
* 选择Minimal，然后下载
* 解压，将sd/bootloader拷贝到switch的sd卡，覆盖bootloader目录
* 打开网站[gbatemp](https://gbatemp.net/threads/sigpatches-for-atmosphere-hekate-fss0-fusee-secondary-only.571543/)下载附件
* 解压到switch的sd卡
* 下载[Awoo](https://github.com/Huntereb/Awoo-Installer)最新版
* 解压到switch的sd卡
* 顺便可以拷贝几个游戏

# 备份系统
TODO

# 虚拟系统
https://switch.homebrew.guide/emummc/emummc.html

# 安装游戏
* 默认是applet mode，按住R打开游戏，则进入full mode


