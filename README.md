## Linux应用安装脚本集合

> 集中Linux应用安装过程中的指令以实现懒人式快速安装.

## Why？

自从切换使用Linux后，就觉得每次到网上搜索安装教程比较费事；

同时，安装步骤有时候五花八门，更是雪上加霜，还容易把源搞坏。

所以，我制作了这个类似应用商店的东西，

并花费了一下午的时间，从列表中所有软件的官网找到了不同系统的安装方式；

然后把一些步骤集合起来，又加上了一些中文说明（如果可能的话）：

做好了这个零技术含量但是工作量比较大的东西。

## How？

首先clone仓库：

```git
git clone https://github.com/wzk0/app-installation-script
```

随后编辑`config.yaml`：

```yaml
##感谢使用！

main:
  pac: apt      ##在此输入包管理器的全称，例如 apt、yum等；强烈建议使用Debian系的系统，因为软件相对而言比较全；
  su: 1		##如果为1， 则执行安装时会以sudo执行；其他值则说明无需sudo；
  ok: 1		 ##如果为1，则说明配置完成；其他值则说明没有完成配置。
```

然后执行`python3 main.py`即可。

> 注意：需要`requests`模块以获取安装脚本。

## About

为了方便及时更新和修复错误，以及添加与删除软件，同时也为了节省空间，我把实际进行安装的脚本放在了另一个仓库： https://github.com/wzk0/repo-of-app ，超级希望大家可以归纳贡献自己安装过程中的步骤，说明一些可能的坑，以及分享更好的软件，从而让Linux得到更好的推广！（说得有点大。。）

另外，安装脚本几乎全部考虑了不同系统的安装方式，以及是否拥有sudo权限，只需要在`config.yaml`中设置即可；但是还是推荐大家使用Debian系的系统，能保证列表中所有软件的安装。

## List

目前已有的软件：

![list](https://raw.githubusercontent.com/wzk0/photo/main/appppppp.png)

准备添加的软件：

* yesplay music
* picgo
* 阿里云小白羊
* 搜狗输入法
* ...

## END

感谢watching的你！