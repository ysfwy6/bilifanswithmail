# 哔哩哔哩粉丝数监测程序

其实就是一个十分简单的python程序，一百来行代码，Releases里有已经编译和打包过的文件（网页版地址[https://shoyu.top/bili](https://shoyu.top/bili)）

### 用法

#### 电脑上没有安装Python且操作系统为64位：

下载Releases里的```bilifanswithmailv0.1-win-x64.zip```并解压，把解压后的目录里的```biliconf.txt.example```改名为```biliconf.txt```并按需修改其中的参数，然后运行```run.bat```即可

参数参考如下（不要直接从这里复制！）：
```
{
    "uid":"229778960",    想要监测的UID，一般填写自己的
    "delay":"30",    刷新延时，单位是秒，默认30，刷新太快可能会被封接口
    "logsave":"",    日志保存文件名，默认为空，程序会自动以“log+日期+时间”的格式命名
    "mailhost":"smtp.qq.com",    SMTP服务器，使用QQ邮箱发件的无需修改，其他服务商需要按照对应的设定进行修改
    "mailuser":"10000@qq.com",    用来发件的邮箱的用户名，一般和邮箱地址相同
    "mailpass":"abcdef",    用来发件的邮箱的密码或授权码，QQ邮箱需要到mail.qq.com下登录并生成授权码，然后填入
    "sender":"10000@qq.com",    发件地址，一般和邮件地址相同
    "receiver":"10001@qq.com",    收件地址，填写用来接收通知邮件的邮箱地址
    "from":"粉丝变化通报",    发件方，可作为邮件标题（手机上通知会以此为标题）
    "to":"shoyu"    收件方，目前无效果，可随意填
}
```

#### 电脑上已经安装Python或操作系统为32位（假定已经安装Python）：

下载仓库根目录的```bilifanswithmail.py```并修改里面的参数比如smtp用户名密码以及收件邮箱等，然后在命令行窗口运行即可

**如果上面的没有看明白的话按第一条走就行了

还有，拆分exe文件保存的原因是因为完整打包的文件会引起windows defender报毒，改了几次源码都一样**
