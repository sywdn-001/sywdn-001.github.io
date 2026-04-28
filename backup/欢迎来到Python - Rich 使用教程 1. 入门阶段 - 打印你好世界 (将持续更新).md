***

>提前说明：本文是一个六年级小学生所写，如有错误请指出，不喜勿喷！
>
>转载请标明出处：十月玩电脑
>
>若有侵权，请联系删除图片或文字：<124463699@qq.com>
>
>Rich 是**Python**里的第三方库，可以再终端里渲染**富文本**，如**您现在正在看的文章**也是我的网站渲染的**Markdown**文本，还不止这些，除此之外，还可以渲染面板、表格等等，今天为大家演示**环境配置和打印函数**
>
>## 准备工作：
>
>如果你想使用`Python - Rich`，需要具备以下条件！
>
>- [x] Windows/Mac操作系统(本文演示Windows10环境)
>- [x] 一个安装了**Python** 和 **pip包管理器** 环境的电脑

***

## Step 1 : 工欲善其事，必先利其器 - 安装 Rich

首先，按下键盘上的**<kbd>Windows</kbd>+<kbd>R</kbd>**键(**同时按下**)，调出运行框：

![1](https://github.com/user-attachments/assets/783c0847-48b3-426d-aaa4-5ee19a36e759)

在`打开(O): `右侧的输入框中输入`Cmd`三个字符，如下图：

![2](https://github.com/user-attachments/assets/ccc781a3-e54d-4417-9acf-726d5acd2f25)

然后按下键盘上的<kbd>Enter</kbd>键，弹出的窗口便是**Windows命令提示符**不要**关掉**，要用！

![3](https://github.com/user-attachments/assets/e607f56e-8ee6-4b07-a8e3-5055789480d8)

因为国内连接接 `Pypi(pip库下载站-服务器在国外)` 的速度令人无法忍受，所以我们先进行**换源工作**(非必须，如果你受得了**下载速度=蜗牛速度的话**)

> [!Warning]
>
> 此操作会将原本的 **Pip源** 替换，谨慎操作！

在打开的窗口里输入`pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`

出现了`Writing to C:\Users\你的用户名\AppData\Roaming\pip\pip.ini`输出即为成功：

![4](https://github.com/user-attachments/assets/6bd25f04-c602-4b02-9907-61fa5f38afcc)

然后输入`pip install rich`命令，**pip包管理器**会自动从镜像服务器拉取**最新版**进行安装，安装完成后，如下图：

![5](https://github.com/user-attachments/assets/e3d334ab-ed52-4076-b7e1-c2130b68708c)

***

## Step2 : 小试牛刀 - 动手写代码

然后打开宇宙级编辑器-`VSCode`，新建一个文件，随意命名，**后缀必须为`.py`**，写上这么一段代码

![6](https://github.com/user-attachments/assets/8cd80319-0600-4d2f-99b4-f90bd5c851e5)

你说**看不清**？

下面有图片和代码(代码可以**直接复制**)



```python
from rich import print
print("[red]Hello World[/red]")
```

当你点击运行按钮，应该输出以下文字：

![7](https://github.com/user-attachments/assets/907ff109-a355-4f9b-9dd4-60c97d4168fa)

**放大**版 -> :

![8](https://github.com/user-attachments/assets/dfe1e6b5-cfb5-4f97-8d18-f552626c686f)

![还是你牛](https://tse1-mm.cn.bing.net/th/id/OIP-C.4U91eIRtZJqVcsjpr_dEIQHaHa?w=185&h=184&c=7&r=0&o=5&dpr=1.3&pid=1.7)

到了这一步，你已经超过了**99.9%**的人，因为你已经动手配置好了**运行环境**，写起了**代码**，知道了**如何运行代码**···

好了，下面让我们理解一下代码含义：

|               代码                |                             解释                             |
| :-------------------------------: | :----------------------------------------------------------: |
|     `from rich import print`      |                      引入**Rich 模块**                       |
|             `print()`             |                    **Rich**的**打印**函数                    |
| `print("[red]Hello World[/red]")` |   使用**Rich**的**打印**函数**输出Hello World**并**标红**    |
|         ``[red]和[/red]``         | **Rich**的**打印**函数的**颜色标识**让Rich知道该将文本**标记成什么颜色** |

好了，至此，全文终！

更多Rich系列文章将在后续发布！