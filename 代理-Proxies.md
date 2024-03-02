# 代理 Proxies

<img width="637" alt="ui-proxies1 a5f01f1e" src="https://github.com/Z-Siqi/Clash-for-Windows_Chinese/assets/77391690/cbdefaea-e0e4-425c-b6ce-8decf9fb93f9">

代理页面主要的作用就是**切换代理模式和切换节点**

## 切换代理模式

Clash 共有三种工作模式：

* 全局（Global）：所有请求直接发往代理服务器
* 规则（Rule）：所有请求根据配置文件规则进行分流
* 直连（Direct）：所有请求直接发往目的地

切换不同模式时，对应的节点列表会对应变化

## 切换节点

> TIP
> 
> 延迟测试(网络图标)可测试所有节点的延迟，可在Settings→Latency Test URL修改测试URL

节点按照策略组分开，并可以以组为单位进行延迟测试，可以方便选出延迟更低的节点。或者可以使用策略组优化逻辑，策略组原理请参考：[策略组原理理解]()
