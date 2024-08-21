# *Milkv-duo-openwrt*
## 此仓库提供VizOS生成的镜像，未使用workflow在线生成(因为不会workflow)，使用本地WSL编译并上传。
#### 在duo256m或者duos镜像生成并烧录后，请使用本仓库提供的 boot.sd 和 fip.bin 替换原sd卡中的 u-boot 文件。这两个文件均由duo-buildroot-sdk官方仓库生成的，源码在官方仓库都可以找到，不存在其他问题。如不放心，可以自己生成uboot并替换。替换之法单纯就是我懒😅，再加上实力不够，不会改u-boot。希望各位有实力的大佬能帮忙补齐这一部分缺失源码的问题。谢谢!
(最新镜像及源码:uboot问题成功修复，最新镜像无需替换uboot了，最新源码使用duo仓库的kernel,可以直接编译烧录启动,不用替换uboot)

可以在menuconfig中勾选apk包管理器,此包管理器经测试可用。可以切换为国内镜像源,使用时会出现报错UNTRUSTED signature，可添加--allow-untrusted参数临时解决.😋
常用的解决方法，官方源输入:apk add -X https://dl-cdn.alpinelinux.org/alpine/latest-stable/main -u alpine-keys  --allow-untrusted
清华源输入:apk add -X https://mirrors.tuna.tsinghua.edu.cn/alpine/latest-stable/main -u alpine-keys  --allow-untrusted

If you are not within China, you can use official-image-site:
```
sed -i 's/mirrors.tuna.tsinghua.edu.cn/dl-cdn.alpinelinux.org/g' /etc/apk/repositories
```
哥哥姐姐们，duos的uboot已经上传，请各位哥哥姐姐查收!😋
