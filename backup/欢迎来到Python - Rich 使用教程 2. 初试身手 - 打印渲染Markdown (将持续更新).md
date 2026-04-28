>提前说明：本文是一个六年级小学生所写，如有错误请指出，不喜勿喷！
>
>转载请标明出处：十月玩电脑
>
>若有侵权，请联系删除图片或文字：<[124463699@qq.com](mailto:124463699@qq.com)>
>
>Rich 是**Python**里的第三方库，可以再终端里渲染**富文本**，如**您现在正在看的文章**也是我的网站渲染的**Markdown**文本，还不止这些，除此之外，还可以渲染面板、表格等等，今天为大家演示**高手的基操**
>
>## 准备工作：
>
>如果你想使用`Python - Rich`，需要具备以下条件！
>
>- [x] Windows/Mac操作系统(本文演示Windows11环境-有钱换电脑了 :(喜 ) 
>- [x] 一个安装了**Python** 和 **pip包管理器** 环境的电脑

***

## Setp1 ：工欲善其事，必先利其器 - 安装Rich

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

## Step2 ：初试身手 - 尝试渲染一段Markdown文本

#### Q: Markdown是什么

##### 	A: `Markdown`是一种被广泛应用的标记性文本语言，在编程和AI技术领域被广泛运用

#### Q: Rich可以渲染Markdown吗？

##### 	A: 可以，但是能力-> 有限 <- 无法为你渲染所有Markdown标签

那么，现在就让我们打开VSCode开始敲代码吧！

先写出万能的引入库代码

```python
from rich.console import * #这个*号代表引入所有功能
```

![1](https://github.com/user-attachments/assets/5ab3934f-8bdc-4b9e-bea3-686265aa89ee)

现在，我们准备一段`Markdown`文本

```markdown
# 这是一级标题
## 这是二级标题
### 这是三级标题
```

将他以**字符串**的形式嵌入到代码里面

```python
from rich.console import * #这个*号代表引入所有功能
###########新增代码###########
md_text = """
# 这是一级标题
## 这是二级标题
### 这是三级标题
"""
###########新增代码###########
```

![2](https://github.com/user-attachments/assets/0a77f874-50f9-4d3c-93eb-e37cea07c2c1)

如果不出意外的话，程序将会运行成功！

![3](https://github.com/user-attachments/assets/a9aa7a51-2311-493d-bc0e-f86389312510)

但是，我们会发现一个问题，程序**什么也没有输出**

这就对了，应为我们还没写输出的代码

```python
from rich.console import Console #这个*号代表引入所有功能
###########新增代码###########
md_text = """
# 这是一级标题
## 这是二级标题
### 这是三级标题
"""
###########新增代码###########
Console.print(md_text) #输出
```



![4](https://github.com/user-attachments/assets/c9ccbc2e-2cf3-4c42-8f4c-b03cc5ad1deb)

点一下**运行**，神奇的事情发生了！

那就是...

![5](https://github.com/user-attachments/assets/d6eb8415-9745-4c4f-90b0-150079d679b3)

你猜对了，那就是... 

**报错！**

不急不急，我们引入下Markdown再修改一下代码

```Python
from rich.console import Console
from rich.markdown import Markdown
###########新增代码###########
md_text = """
# 这是一级标题
## 这是二级标题
### 这是三级标题
"""
###########新增代码###########
console = Console()
md = Markdown(md_text)
console.print(md)


```



![Image](https://github.com/user-attachments/assets/1568aa72-e928-43ce-94d3-77ca4d1eee39)

**成功！**

## Setp3 ：结语

谢谢您看完本文章，看完之后记得动手实践一下哦！