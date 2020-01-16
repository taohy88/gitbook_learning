# Win10

```
win10 截图快捷键 shift+win+s

gpedit.msc//组策略
mscconfig.exe //启动项设置
net stop sharedaccess //关闭防火墙
net start sharedaccess//开启防火墙
远程桌面的命令 mstsc
netsh advfirewall

1.解决window update无法工作的问题，将导致.Net framework 4 无法安装
net stop WuAuServ //停用window update 服务
windows/SoftwareDistribution 重名名
net start WuAuServ//启用window update服务
//----------------------------------------------------------------------

2.ping规则启用和禁止的解决方案
netsh firewall set icmpsetting 8
netsh firewall set icmpsetting 8 disable
//-----------------------------------------------------------------------

3.解决window fire无法打开 0x6D9

NT Service/MpsSvc 帐户需要以下项的权限：

HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/SharedAccess/Epoch
查询值 ； 设置值

HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/SharedAccess/Parameters/FirewallPolicy
完全控制 ； 读取

HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/SharedAccess/Defaults/FirewallPolicy
完全控制 ； 读取


为 DHCP 客户端服务如果"NT Service/DHCP"帐户不具有对以下项所需的权限可能会出现此问题：

注册表项：
HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/Dhcp
所需的权限： 查询值，创建值枚举子项，通知，读取控制

注册表项：
HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/Dhcp/Configurations
所需的权限： 完全控制、 读取


"诊断策略服务"服务帐户 Trustedinstaller 缺少以下项的权限时可能会出现该问题：

HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/DPS/Parameters
所需的权限： 完全控制、 读取
说明：

在这些注册表项中添加帐户的权限。例如对于下面是 Windows 防火墙服务的步骤：

1.在注册表编辑器浏览到要添加的权限项。
2.右键单击键，然后单击权限。
3.请确保位置选择要在本地计算机。
4.在"输入对象名称来选择字段中，键入"NT SERVICE/mpssvc"。然后单击检查名称。
5.单击确定。
6.然后在列表中选择将出现该帐户，并添加对其进行适当的权限。
7.单击确定。


4.解决两个网卡冲突的问题
    route print 查看路由表
    route add 0.0.0.0 mask 0.0.0.0 192.168.1.1(网关1) -p
    route add 192.168.2.0 mask 255.0.0.0 192.168.2.1(网关2)

5.远程桌面的命令 mstsc


忘记密码：
1、重新启动计算机，在启动画面出现后马上按下F8键，选择“带命令行的安全模式”。
  2、运行过程结束时，系统列出了系统超级用户“administrator”和本地用户“zhangbq”的选择菜单，鼠标单击“administrator”，进入命令行模式。
  3、键入命令:“net user zhangbq 123456 /add”，强制将“zhangbq”用户的口令更改为“123456”。若想在此添加一新用户(如:用户名为abcdef，口令为123456)的话，请键入“net user abcdef 123456 /add”，添加后可用 “net localgroup administrators abcdef /add”命令将用户提升为系统管理组“administrators”的用户，并使其具有超级权限。
  4、重新启动计算机，选择正常模式下运行，就可以用更改后的口令“123456”登录“zhangbq”用户了。另外，zhangbq 进入 登入後在〔控制台〕→〔使用者帐户〕→选忘记密码的用户，然後选〔移除密码〕後〔等出〕 在登入画面中选原来的用户便可不需密码情况下等入 (因已移除了) 删除刚才新增的用户，在〔控制台〕→〔使用者帐户〕→选〔alanhkg888〕，然後选〔移除帐户〕便可
```

