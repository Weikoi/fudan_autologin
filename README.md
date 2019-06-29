# fudan_autologin
复旦大学校园网自动登录联网脚本。

解压到D盘，然后选中login.bat并编辑：

```
    D:\curl-7.62.0-win64-mingw\bin\curl http://10.108.255.249/include/auth_action.php -d "action=login&username=******&password=******&ac_id=1&ajax=1"
```
把username=****** 中的 ****** 替换成自己的学号
把password=****** 中的 ****** 替换成自己的密码

前面的D:\是默认你解压到D盘根目录，如果你解压到其他目录，也要随之替换。

现在这个bat脚本双击运行即可登录校园网，你要做的就是用windows 计划任务中去设置成自动运行就好。

一般设置成开机自动运行，如果你是需要整夜爬虫，那么要注意复旦的校园网断网是在凌晨3点零几秒。所以我设置的是三点三十秒自动执行这个脚本，爬虫程序也要有断网重爬的功能。

当然如果你用的是linux，那么用crontab去执行脚本中的curl命令就好，相信用Linux的小伙伴应该不用多解释啊。

enjoy it!