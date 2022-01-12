# 技嘉B460M D2V主板 Montery 黑苹果EFI文件分享

> 作者：Kingtous

实际需要，鉴于技嘉的B460m没有多少合适的EFI使用，于是自己动手配了个EFI使用。

![PNG](https://s2.loli.net/2022/01/09/35i2rEWZR8N4da9.png)

## 已经工作 Working

- CPU：Intel 10400（睿频已修正1GHz-4GHz，完美）
- 显卡：Intel UHD 630（已经完美驱动，可以使用dvi-hdmi）
    - 2022.01.12：（此主板集成显卡无HDMI输出，但是可以通过DVI转HDMI）修正framebuffer，换用0000 id，修复dvi转hdmi后紫屏问题
- 独立显卡：GTX 1660s（已屏蔽）
- 网卡：主板板载，正常工作
- USB：目前定制前面所有+后面4个USB3.0接口
- 睡眠：正常唤醒
- 声卡：ALC887。未测试，默认layout-id=1

## 安装步骤
- EFI内完善SMBIOS信息（序列号等）
- BIOS中切换至集成显卡
- 正常安装Hackintosh即可

## 待解决 TODO

不是刚需，随缘更新解决

[ ] USB 3.0（已经打入补丁但无效，待排查问题）
- EFI内含有USBMap.kext以及USBPorts.kext。（目前默认使用基于USBMap制作的定制USB端口，目前发现插入3.0 u盘还是走的2.0。USBPorts.kext目前可以加入SS0x USB端口，可以识别出3.0设备，但是U盘图标出不来。为了保证功能性，先使用USBMap）


## 贡献

欢迎完善EFI～如果我的工作帮助到了你，不妨点个🌟支持一下。
