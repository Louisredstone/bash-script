若想知道您的操作系统支持哪些 Shell 类型，可在终端中输入命令：
```
$ cat /etc/shells
```
若想知道 Bash 的绝对路径，可在终端中输入命令：
```
$ which bash
```

------

## Bash脚本的创建

使用cd命令进入将要保存脚本的目录。使用文本编辑器（如gedit/vi/vim命令），并键入shell命令<br>
使用touch命令创建脚本<br>
```
touch file_name
```
在文本编辑器中打开脚本,键入以下命令（编辑器命令可根据个人更改）<br>
```
gedit file_name.sh
```
脚本的第一行一般如下：<br>
```
#!/bin/bash
echo "Hello World!"
```
注：

#!（SheBang）是一个约定的标记（解释器指令），它告诉系统这个脚本使用哪一种Shell
echo是Bash中的内置命令，用于通过传递参数来显示标准输出，将文本或字符串打印到屏幕上。

------

## Bash脚本的运行

作为可执行程序
```
chmod +x ./file_name.sh
./file_name.sh
```
注：

第一行给予脚本执行权限<br>
第二行执行脚本

作为解释器参数
```
/bin/sh file_name.sh
```
注：

该方式不需要在第一行指定解释器信息

第二种方式似乎不行。

------

## 字符串

当您输入的内容为简单的字符串或文本时，单引号和双引号的作用没有任何区别。请仔细阅读以下示例：
```
#!/bin/bash
echo 'Hello World!'
echo
echo "Welcome to W3Cschool!"
```
执行结果：
```
$ ./bash_script.sh
Hello World!
Welcome to W3Cschool!
```

## 变量

当您想打印输出一个已定义的变量，则需要使用双引号。这时若使用单引号不会将其视为变量。请仔细阅读以下示例：
```
#!/bin/bash
comment="Welcome to W3Cschool!"
echo "$comment"
echo '$comment'
```
执行结果：

$ ./bash_script.sh
Welcome to W3Cschool!
$comment