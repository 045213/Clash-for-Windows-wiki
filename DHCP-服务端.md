# DHCP 服务端

## 版本要求

0.16.0 版本更新后，macOS 版本支持 DHCP 服务端部署

## 用途

[TUN 模式](https://github.com/Z-Siqi/Clash-for-Windows_Chinese/wiki/TUN-%E6%A8%A1%E5%BC%8F)下，macOS 可作为局域网代理网关。DHCP 服务器可以方便对局域网内其他设备进行地址及网关分配，进而控制设备流量是否被 Clash 接受并处理。

## 开启条件

1. [TUN 模式](https://github.com/Z-Siqi/Clash-for-Windows_Chinese/wiki/TUN-%E6%A8%A1%E5%BC%8F)正确配置并运行，并且已经开启 IP 转发
2. 网络中 DHCP 功能关闭（一般是路由器，避免冲突）
3. 本机 IP 地址设置为静态地址

## 操作步骤

1.进入 Settings 界面，底部找到 `Experimental Features` 打开 `DHCP Server` 选项

2.进入 Router 界面，点击右上角 Start 按钮
<img width="850" alt="dhcp1 476ebb29" src="https://github.com/Z-Siqi/Clash-for-Windows_Chinese/assets/77391690/476eefb0-dd18-4555-9db5-8125b87e768b">

点击 Interface 右边选择对应网卡，此时剩下值会自动填充，如果不明白这些字段的意义，使用默认即可

3. 点击 Continue 后，DHCP 服务器将会启动
<img width="850" alt="dhcp2 9811b06a" src="https://github.com/Z-Siqi/Clash-for-Windows_Chinese/assets/77391690/744ef897-d325-4ade-bd1f-5c7b7d9325f8">

局域网中设备重新连接后，列表中将会出现。此时可以在 `Default Gateway` 和 `Clash TUN` 中切换进而控制设备是否由 Clash 接管网络，切换后设备需要重新接入网络

> TIP
> 
> 接管切换后需要将设备重新接入网络方能获取正确的地址

> TIP
> 
> 启动 DHCP 服务端功能后，CFW 将会阻止系统进入休眠（但允许关闭显示器）