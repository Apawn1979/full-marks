# 查看/修改系统支持的shell

```shell
# 查看系统支持的shell风格
$ cat /etc/shells

# 查看当前系统默认的shell
$ echo $SHELL

# 查看当前使用的shell
$ echo $0

# 将系统默认shell切换为zsh
$ chsh -s /bin/zsh

# 切换成bash
$ chsh -s /bin/bash
```









