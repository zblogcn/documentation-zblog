# 下载安装

更新时间： {docsify-updated}

## 环境要求

IIS：建议7.0+

数据库：`Access` / `MSSQL`

## 下载地址

下载入口页：[https://www.zblogcn.com/zblog/](https://www.zblogcn.com/zblog/ "Z-Blog，ASP博客程序与建站系统")

- [Z-BlogASP 2.3正式版直链下载](https://www.zblogcn.com/program/zblog23/ "Z-Blog 2.3 Avengers Build 180518")

- [单文件在线安装程序](http://bbs.zblogcn.com/thread-76062-1-1.html "Z-BlogASP在线安装程序")

## 安装教程

1. 打开 “服务器管理器”，在服务器管理器中，选择 “添加角色和功能”。

2. 在 “开始之前” 页面，点击 “下一步”。

3. 选择“基于角色或基于功能的安装”，点击下一步，

4. 服务器选择默认即可（从服务器池中选择服务器>选择本机），点击下一步，

5. 在 “服务器角色” 列表中，展开 “Web 服务器（IIS）”，选择 “Web 服务器” 选项，此时会弹出 “添加功能” 对话框，点击 “添加功能”，手动选择Web服务器（IIS）下的所有组件。点击下一步

6. 功能默认无需变动，点击下一步

7. 勾选“如果需要，自动重新启动目标服务器”，在弹出的对话框点击“是”，然后点击安装

8. 安装Microsoft SQL Server 2022 https://www.microsoft.com/en-us/sql-server/sql-server-downloads 建议下载Developer版本。

下载的应该是这个：

双击运行，点击基本安装

接受许可协议

选择安装位置

等待安装完成

9. 建议安装Microsoft SQL Server Management Studio https://learn.microsoft.com/zh-cn/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16 便于对数据库进行操作。

点击此处下载

下载的是这个：

打开后点击安装。

10. 在开始菜单找到打开SQL Server Management Studio 20，登录数据库，设置SQL Server服务器身份验证为“SQL Server 和 Windows身份验证模式”

打开SQL Server Management Studio 20

登录到Microsoft SQL数据库

其他默认，注意这里“加密”选择“可选”，点击连接

连接后右键你的服务器，点击属性

修改身份验证为“SQL Server 和 Windows身份验证模式”，点击确定。

11. 创建一个名字为“zblog”的数据库，并且在安全性中创建一个登录名，设置为SQL Server身份验证模式并设置密码，服务器角色为public、sysadmin。

在数据库右键，点击新建数据库

命名为zblog，点击确定

创建登录名

1.设置登录名（用户名）

2.选择“SQL Server 身份验证”

3.设置密码（密码应符合最低安全要求）

4.不勾选“强制密码过期”

5.选择默认数据库为zblog

服务器角色中勾选“public、sysadmin”

用户映射中勾选zblog

操作完成后，点击确定。

12. 在https://update.zblogcn.com/zip/Z-Blog_2_3_Avengers_180518.zip下载ZBlog ASP源码，将其上传并解压到服务器（建议解压到C盘根目录）

13. 在IIS中点击新建网站，选择解压好的的网站源码，配置好IP和端口，在ASP中设置启用父路径为True

在开始菜单>Windows管理工具里找到IIS，

在“网站”右键，点击添加网站

1.网站名称随便起一个就行

2、3、4：选择解压好的zblog源码

5.修改成未被占用的端口

6.点击确定

在刚刚创建好的网站里，点击ASP

设置启用父路径为True（重要！必须设置）

14. 浏览器访问 http://127.0.0.1:你设定的端口/zb_install/

15. 根据指示安装ZBlog。
