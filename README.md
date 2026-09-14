# atmosphere-switch
大气层switch使用指南

# 准备
* 可以软破的switch（未熔断/非续航受补丁限制机型）
* RCM短接器及注入器（或手机/电脑注入工具）
* TF/SD卡（推荐格式化为 FAT32 格式，稳定性最好）

# 准备SD卡
* 下载 [Atmosphere (大气层)](https://github.com/Atmosphere-NX/Atmosphere/releases) 最新版
* 把 `atmosphere-xxxxxx+hbl-xxx+hbmenu-xxx.zip` 解压到 SD 卡根目录
* 在同版本发布页面下载 `fusee.bin`
* 下载 [hekate](https://github.com/CTCaer/hekate/releases) 最新版
* 把 `hekate_ctcaer_xxxx_Nyx_xxx.zip` 解压到 SD 卡根目录
* 把刚才下载的 `fusee.bin` 放到 SD 卡的 `bootloader/payloads/` 目录
* 把本工程的 [hekate_ipl.ini](./hekate_ipl.ini) 拷贝到 SD 卡的 `bootloader/` 目录
* 把 RCM 注入器插入电脑（识别为 U 盘）：
  * 打开 `\ATMOSPHERE_HEKATE` 目录，把 hekate 压缩包内的 `hekate_ctcaer_xxx.bin` 重命名并覆盖为 `payload.bin`，然后拔出注入器
* 下载 [sys-patch](https://github.com/impeeza/sys-patch/releases)（用于自动给系统打签名补丁，支持安装和运行 NSP/XCI 游戏），解压到 SD 卡根目录
* （推荐）下载主流游戏安装管理工具 [DBI](https://github.com/rashevskyv/dbi/releases)，将 `DBI.nro` 放入 SD 卡的 `switch/DBI/` 目录下
* （可选）下载叠加层加载工具 [nx-ovlloader](https://github.com/WerWolv/nx-ovlloader/releases) 解压到 SD 卡；下载快捷菜单叠加层 [Tesla-Menu](https://github.com/WerWolv/Tesla-Menu/releases) 的 `ovlmenu.ovl` 放入 SD 卡 `switch/.overlays/` 目录
* （可选）下载金手指工具 [EdiZon-Overlay](https://github.com/proferabg/EdiZon-Overlay/releases) 的 `EdiZon.ovl` 放入 `switch/.overlays/` 目录；或使用 [EdiZon](https://github.com/WerWolv/EdiZon/releases)
* （可选，防Ban设置）把本工程的 [default.txt](./default.txt) 拷贝到 SD 卡的 `atmosphere/hosts/` 目录（若无 hosts 目录请手动新建），阻断任天堂服务器域名，防止虚拟系统联网导致Ban机

# 启动
* 长按电源键 10 秒以上强制关机
* 右手柄滑轨底部插入短接器，按住“音量+”键不放，再按一下“电源键”，即可进入 RCM 模式
* 长按 RCM 注入器的 `+` 号按键切换到大气层模式（通常为蓝灯闪烁）
* 将注入器插入 Switch 底部的 Type-C 口，屏幕即刻点亮并进入 Hekate 引导界面
* （推荐）在 Hekate 界面中进入 `Tools` 进行原始系统 eMMC 完整备份，并在 `Tools -> Partition SD Card` 进行 SD 卡分区创建 emuMMC（虚拟系统）
* 在 `Launch` 界面点击 `CFW - emuMMC` 启动虚拟系统

# 安装游戏（推荐使用 DBI MTP 模式）
1. **启动 Homebrew Launcher (HBL)**：
   * **强烈推荐**：按住手柄的 **R 键** 不放，点击主界面的**任意一个已安装游戏**打开，即可进入全内存模式 HBL（避免在相册 Applet 模式下因内存受限导致大型游戏安装闪退或报错）。
2. **使用 DBI 安装游戏**：
   * 打开 **DBI** 工具，选择 **`Run MTP Responder`**。
   * 使用 Type-C 数据线将 Switch 连接到电脑，电脑会直接弹出一个名为 `Switch` 的驱动盘符。
   * 进入该盘符下的 **`5: SD Card install`** 文件夹。
   * 直接在电脑上把游戏安装包（`.nsp`、`.nsz`、`.xci` 等）复制/拖入该文件夹中，DBI 会在 Switch 屏幕上实时显示安装进度，传输完毕即自动安装完成。
   * 安装完成后在 Switch 上按 `X` 退出 MTP 模式即可在主界面畅玩。

*(注：旧版的 Awoo-Installer 及 ns-usbloader 方案在新版系统中兼容性较弱，已逐步被 DBI MTP 直连方案取代。)*
