# 环境搭建
如果希望快速使用，可以[下载](link)我们的已经配好环境的ubuntu虚拟机镜像
## ubuntu
在ubuntu终端输入以下命令
```
sudo apt-get install subversion g++ zlib1g-dev build-essential git python rsync man-db
sudo apt-get install automake m4 flex bison bzip2 patch pkg-config 
sudo apt-get install libncurses5-dev gawk gettext unzip file libssl-dev wget zip time
```

# 源码下载
```
git clone https://git.openwrt.org/openwrt/openwrt.git/
cd openwrt


```
# 编译相关工具下载（TODO: 合并到git）
```
./scripts/feeds update -a
./scripts/feeds install -a
```
# 编译
## 配置
```
make menuconfig
“Target System” ⇒ “Atheros AR7xxx/AR9xxx”
“Target Profile” ⇒ “TP-LINK TL-WR841N/ND v11”
make defconfig
make
```
## 编译`make -j4`
> 第一次编译请使用`make`

# 烧写
## 全烧写
## 升级
- luci网页升级
- uboot网页升级
- uboot tftp升级

# 相关参考资料
- [openwrt 官网](https://openwrt.org/) 
- [openwrt 中文网站](http://www.openwrt.org.cn/) 
- [openwrt 论坛](http://www.openwrt.org.cn/bbs/forum.php) 
