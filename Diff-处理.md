# Diff 处理

Diff 处理即对配置文件进行三路合并，允许在不使用[配置文件预处理](https://github.com/Z-Siqi/Clash-for-Windows_Chinese/wiki/%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%E9%A2%84%E5%A4%84%E7%90%86)的情况下，保留对配置文件的修改并应用到下次更新。

0.18.4 版本更新后，支持使用 Diff 方式处理配置文件。

如果你熟悉 Git，此方式类似于`git merge`。

## 使用方法

1. 进入 Profiles 界面，在需要设置 Diff 处理的配置文件右侧三点图标悬停，出现菜单后，点击构建 Diff 文件图标：

<img width="193" alt="diff1 8e879692" src="https://github.com/Z-Siqi/Clash-for-Windows_Chinese/assets/77391690/fe1b291a-bba1-4309-95ab-c88be1b8354f">
<img width="435" alt="diff2 cf612d69" src="https://github.com/Z-Siqi/Clash-for-Windows_Chinese/assets/77391690/a5e03c30-635c-474f-ad24-529c0bcd3233">

2. 此时会调用系统默认编辑器编辑配置文件，对此文件的编辑将会在配置文件更新时自动合并到新的配置文件中

3. 更新一次配置文件

## 冲突

如果远端配置文件发生更新，并且与本地修改产生冲突，将需要手动进行合并。

冲突的格式非常简单：
```
<<<<<<<
  本地修改
=======
  远端修改
>>>>>>>
```

根据自己的需求，把多余的地方删除即可，包括`<<<<<<<`、`=======`和`>>>>>>>`。

如果使用 VSCode，操作更简便：

<img width="741" alt="diff3 e0affcae" src="https://github.com/Z-Siqi/Clash-for-Windows_Chinese/assets/77391690/bea51a7d-954f-4728-92a4-dadcb4f0a5b6">

> TIP
> 
> Diff 处理会在预处理之后进行
