# justsoso
# 郑大健康状况上报平台脚本

## ❗功能
使用Actions执行脚本，每天4点定时签到，无需手动运行，签到成功后会发送邮件到你的私人邮箱。模拟手动操作，防止登录失效。
关于安全性：学号和密码和邮箱用Secrect进行保存，复制项目到自己到账号下不会导致任何人的密码泄露。
**注意：项目启用后60天无更新时，Actions功能会自动关闭，届时需要再次手动开启。**

---
## ❓部署
### 1. Fork 仓库
   * 首先要自己注册一个github账号，然后将此项目fork的自己的仓库
   * 点击页面右上角的`Fork`按钮，将本项目保存到自己的仓库。点击`Fork`左侧的`Star`键可以表示您对本项目和作者的认同。🤩
   ![fork.PNG](https://i.loli.net/2020/11/24/2hTtGldiZF9B7DX.png)
### 2. 添加 secrets
   * 点击`Settings`-->`Secrets`-->`New repository secret`，进入新建页面。
   ![secrets.PNG](https://i.loli.net/2020/11/24/mIWLRTzUJxuiMHa.png)
   * 在`Name`栏输入`UID`，`Value`栏输入自己的学号，然后点击`Add secret`。
   * 再次点击`Settings`-->`Secrets`-->`New repository secret`，进入新建页面。
   * 在`Name`栏输入`UPW`，`Value`栏输入自己的登录密码，然后点击`Add secret`。
   * 第三次点击`Settings`-->`Secrets`-->`New repository secret`，进入新建页面。
   * 在`Name`栏输入`MAIL_USERNAME`，`Value`栏输入自己发送邮件的邮箱，然后点击`Add secret`。(**注意：此处默认使用QQ邮箱发送邮件，如果想使用其他邮箱，请自行在main.yml文件中修改参数。**)
   * 第四次点击`Settings`-->`Secrets`-->`New repository secret`，进入新建页面。
   * 在`Name`栏输入`MAIL_PASSWORD`，`Value`栏输入自己发送邮件的邮箱的密码，然后点击`Add secret`。(**注意：* * QQ邮箱的密码并非登录密码，而是QQ邮箱授权码，MAIL_PASSWORD不是发送邮箱账号的密码，！！！，是授权码，登录QQ邮箱，登录后点击`设置`然后进入`账户`将‘POP3/IMAP/SMTP/Exchange/CardDAV/CalDAV服务’中的服务开启，获取授权码，将授权码填入即可。**)
   * 第五次点击`Settings`-->`Secrets`-->`New repository secret`，进入新建页面。
   * 在`Name`栏输入`receive_MAIL`，`Value`栏输入自己接收填报成功邮件推送的邮箱，然后点击`Add secret`。
   * 多人模式与单人模式的添加方法相同，具体格式为`学号,学号,学号`和`密码,密码,密码`，例如：`201884160000,201884160001`和`12345678,12345678`(**注意：逗号为英文标点，使用中文标点会导致脚本运行失败**)。
### 3.启用 Actions
   * 点击上方的`Actions`，点击绿色按钮确认启用`Actions`功能。
   * 点击左侧`justsoso`，点击`Run workflow`，运行一次项目。
   ![actions.PNG](https://i.loli.net/2020/11/24/HrQoCwFkgcAYjps.png)

项目部署完毕后，可以在自己填写的邮箱中查看打卡成功的邮件推送，可以在`Actions`页面点击`View workflow file`查看结果。
![check.PNG](https://i.loli.net/2020/11/24/GUEgdrmpIAxlPW5.png)
如有疑问可通过`Issues`功能提交问题，如出现签到失败的问题请耐心等待更新。

---
## 📢更新方法
   * 点击`Settings`-->`Options`-->`Dangerous Zone`-->`delete this reposity`，按照提示删除本项目，然后重新部署
   * 使用git，相关命令请自行搜索。
# 在大佬的基础上增加了邮件提醒功能
   * 在[@d6imde9](https://github.com/d6imde9)书写的代码基础上添加了邮件推送的功能，将打卡成功的界面利用邮件推送，配置方法已经在上方作了说明
   * 在secrets中增加邮箱账号和密码MAIL_USERNAME和MAIL_PASSWORD，receive_MAIL
   * receive_MAIL为接收邮件的邮箱，EMAIL_PASSWORD不是发送邮箱账号的密码，！！！，是授权码，以QQ邮箱为例，登录后点击`设置`然后进入`账户`将‘POP3/IMAP/SMTP/Exchange/CardDAV/CalDAV服务’中的服务开启，获取授权码，将授权码填入即可
# 特别感谢

 * [@d6imde9](https://github.com/d6imde9)
