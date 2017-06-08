# mono 在线实验环境

## 软件简介

软件基本信息，License，所属的类别，作用，特点等。

Mono是一个由Xamarin公司（先前是Novell，最早为Ximian）所主持的自由开放源代码项目。该项目的目标是创建一系列匹配ECMA标准（Ecma-334和Ecma-335）的.NET工具，包括C#编译器和通用语言架构。与微软的.NET Framework（共通语言运行平台）不同，Mono项目不仅可以运行于Windows系统上，还可以运行于Linux，FreeBSD，Unix，OS X和Solaris，甚至一些游戏平台，例如：Playstation 3，Wii或XBox 360。

所属类别是编程语言

特点:

方便实用

## 软件官网

http://www.mono-project.com/

## Dockerfile 使用方法

Dockerfile在您的Mono应用程序项目中创建一个

此示例Dockerfile将运行一个可执行文件TestingConsoleApp.exe。

FROM mono:3.10-onbuild

CMD [ "mono",  "./TestingConsoleApp.exe" ]

将此文件放在应用程序的根目录中，并在.sln解决方案文件旁边。修改可执行名称以匹配您要运行的内容。

此图像包括ONBUILD添加您的应用程序源代码的触发器/usr/src/app/source，还原NuGet软件包并编译应用程序，将输出放置在其中/usr/src/app/build。

使用Dockerfile，您可以使用应用程序构建和运行Docker映像：

$ docker build -t my-app .

$ docker run my-app

您现在应该会看到应用程序的任何输出。

## 资源链接

- http://www.mono-project.com/
