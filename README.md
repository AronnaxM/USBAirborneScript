# USBAirborneScript

**Autorun.inf file for USBAirborne**

此项目基于[Push3AX/USBAirborne ](https://github.com/Push3AX/USBAirborne '点击前往原项目地址')

此Repo用于存储USBAirBorne相关的代码(修改过的Autorun.inf)、实验结果等。

## 此Repo仅供学习参考USBAirborne工具的相关用法,请勿用于其他途径。使用者行为与此Repo作者无关。


### 0x0 Autorun.inf 

有关 Autorun.inf 的配置条目，Microsoft 官方已经给出，可以参考以下链接：
[https://learn.microsoft.com/zh-cn/windows/win32/shell/autorun-cmds](https://learn.microsoft.com/zh-cn/windows/win32/shell/autorun-cmds)

### 0x1 图标

在Usbairborne插到电脑上时，在文件资源管理器中显示出的图标由Autorun.inf中的 icon 参数决定。其中，图标不局限于原作者示例中给出的可移动磁盘图标 "c:\windows\system32\shell32.dll,79"，也可以替换成其他任意系统自带的或是Usbairborne内存储的 * .exe 程序的图标，如果是前者，可选的系统图标文件位置包括但不限于： 

```ini
c:\windows\system32\imageres.dll
c:\windows\system32\shell32.dll
c:\windows\system32\ddores.dll 
c:\windows\system32\pifmgr.dll
c:\windows\system32\explorer.exe 
c:\windows\system32\accessibilitycpl.dll
c:\windows\system32\moricons.dll
c:\windows\system32\mmcndmgr.dll
c:\windows\system32\mmres.dll
c:\windows\system32\netshell.dll 
c:\windows\system32\networkexplorer.dll
c:\windows\system32\sensorscpl.dll
c:\windows\system32\setupapi.dll
c:\windows\system32\wmploc.dll
c:\windows\system32\wpdshext.dll
c:\windows\system32\compstui.dll
c:\windows\system32\ieframe.dll

```


### 0x2 设备名称

可以设置一个和图标相配合的名称，例如若图标为MP3，那么可命名为便携式音频设备。

***注意，如果含有中文字符，Autorun.inf 必须 ANSI 的形式保存，否则右键菜单乱码。***

### 0x3 自动执行的文件

可执行文件不建议多套一个文件夹，另外可以自动执行 * .bat , * .com , 是否可执行 * .ps1 待定，但是执行 * .ps1 脚本的前提是允许自动执行脚本（因此实战并不不可行），运行如下 PowerShell 命令以启动：

```powershell
set-executionpolicy -executionpolicy unrestricted
```

### 0x4 To be continued . . .
