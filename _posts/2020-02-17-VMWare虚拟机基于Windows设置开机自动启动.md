---
layout: post
title: 'VMWare虚拟机基于Windows设置开机自动启动'
date: 2020-02-17
author: nidoto
cover: 'https://pic4.zhimg.com/v2-873ce86c4330a3acb60848c60e40c064_1200x500.jpg'
tags: 
- Windows
- VMWare
- 软件
- 黑群晖
---
我在虚拟机中安装了黑群晖

然后将物理机上的磁盘直接映射在群晖中使用

所有的文件文件夹在windows中做到随取随用

通过网页传到群晖上的文件也会自动放在物理机上

嗯，确实很香

然后开机设置通过批处理让VMWare和虚拟机的开机自启动

方法如下

第一步：在重要的地方创建一个空白的txt文件取名vm_start.txt

第二步：找到VMWare安装的路径，复制路径，打开txt文件，添加内容加上英文引号。

第三步：打开虚拟机安装的位置，复制路径，添加到txt文件中

格式如下：

"VMWare虚拟机的安装程序"  -x  -- "虚拟机的完整安装路径"

例子：

"C:\Program Files (x86)\VMware\VMware Workstation\vmware.exe" -x -- "E:\DNS服务器\DNS服务器.vmx"
exit

第五步：将vm_start.txt文件的后缀  .txt  改成  .bat  并确认保存。

第六部：按win+R键调出“运行”输入shell:startup回车

第七步：将vm_start.bat文件复制进这个文件夹就OK了

第八步：重启windows系统后，系统自动开启虚拟机里的虚拟机



