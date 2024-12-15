## 介绍

screen是窗口管理器的命令行界面版本，它提供了统一的管理多个会话的界面和相应的功能。当我们开启screen后，只要screen进程没有终止，其内部运行的会话都可以恢复。即使网络连接中断，用户也可以重新进入已开启的Screen中，对中断的会话进行控制，包括恢复或删除。



## 使用教程

1.   安装screen
2.   使用screen

```bash
screen -ls			# 查看当前已有的screen (Attached表示该screen已被连接)
screen -S [name]	# 新建一个名为[name]的screen
screen -r [name]	# 恢复未被连接的名为[name]的screen
```

新建或恢复screen后即可正常输入命令或运行程序，即使关闭本地窗口也可通过screen -r命令进行恢复。

3.   其它命令

```bash
screen -d [name]			# 断开当前连接的名为[name]的screen 
screen -d -r [name]			# 断开当前连接的screen，并进入名为[name]的screen
screen -x [name]				# 恢复之前离线的指定session
screen -X -S [name] quit		# 删除指定的名为[name]的session
```





## 常见问题