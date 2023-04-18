---
layout:       post
title:        "Obsidian使用github作为图床"
author:       "Hux"
header-style: text
catalog:      true
tags:
    - Obsidian
    - Picgo
encoding: GBK
---

![獭](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/17/獭_22-05-03.jpg)

这个最近也是受女朋友的安利，把自己的周报日报和工作进度从Notion转入到了Obsidian中，没什么特别多的理由，虽然Obsidian的看板不好用，没有Notion那么好用的database，但它是离线的这一点就已经足够了，运行速率杠杠的。
转过来之后有些文章也懒得再打开Typora写了，使用Obsidian的插件自动重命名还有丰富的日历插件、模板插件，这都能帮我快速地搭建好一篇新文章的架构。
当然之前的图片和附件我都是默认存放到Obsidian vault本地的一个文件夹中的，但是存在本地不利于多设备同步，图片和附件比较臃肿，于是我就想让Obsidian也使用github作为图床。

## 建立图床repo和准备Token
没什么好说的，去自己的github新建一个repo，名字随意，可以叫xxx-picbed，放在那就好了。
像在Typora里准备图床一样，去你自己github settings页面找到Developer settings，然后生成一个token，new token我还不会用，还是用经典的吧。

![](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/12/2023-04-12_%E4%BD%BF%E7%94%A8github%E4%BD%9C%E4%B8%BAObsidian%E5%9B%BE%E5%BA%8A-20230412_17-33-42.png)
这里权限把repo的权限勾上就行。
![2023-04-12-使用github作为Obsidian图床-20230412-1](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/12/2023-04-12_%E4%BD%BF%E7%94%A8github%E4%BD%9C%E4%B8%BAObsidian%E5%9B%BE%E5%BA%8A-20230412-1_17-33-42.png)
确定之后得到token，复制下来留着一会放到picgo-core的配置文件中。

## Picgo-core设置
### 安装Picgo-core
先安装node-js
安装好之后去terminal里运行
`npm install picgo -g`
安装好之后运行
`picgo -v`看是否有版本号输出，如果有的话代表picgo环境变量已经生效。
### 安装插件
去terminal里安装
`picgo-plugin-github-plus`和`picgo-plugin-rename-file`这两个插件，安装命令是
```
picgo install github-plus
picgo install rename-file
```
将会看到如下输出：
![2023-04-12\_使用github作为Obsidian图床-20230412-2](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/12/2023-04-12_%E4%BD%BF%E7%94%A8github%E4%BD%9C%E4%B8%BAObsidian%E5%9B%BE%E5%BA%8A-20230412-2_17-33-42.png)
到这里插件就安装完成了。
### Picgo-core配置文件
下面进入对picgo-core进行配置，首先打开PicGo-Core配置文件config.json，填入相关配置信息。
> Linux 和 macOS 下配置文件位置为`~/.picgo/config.json`。
>
> Windows 则为`C:\Users\你的用户名\.picgo\config.json`。

我有一份现成的配置：[GitHub - Ryushane/Picgo-config-file](https://github.com/Ryushane/Picgo-config-file)
下载后把config.json文件扔到配置文件的位置，更改里面的token / username / reponame / port等信息，改成你自己的token，github用户名，repo名和代理服务器的http端口。
### 测试上传
首先在自己的terminal试一下，复制一张图片到剪切板，然后去terminal运行：
`picgo u`
应该会得到上传成功的消息。
## Obsidian插件下载
去Obsidian三方插件市场下载image auto upload plugin，安装后启动，把默认上传器改成picgo-core就可以使用了。
![2023-04-12_使用github作为Obsidian图床-20230412-3](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/12/2023-04-12_%E4%BD%BF%E7%94%A8github%E4%BD%9C%E4%B8%BAObsidian%E5%9B%BE%E5%BA%8A-20230412-3_17-33-42.png)