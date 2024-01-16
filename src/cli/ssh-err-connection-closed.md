# ssh 拉取 github 时报错

## 报错（冒号后面部分略有差异）：
```shell
kex_exchange_identification: Connection closed by remote host
```
## 解决
1. 关掉梯子
2. 将 Github 的连接端口从 `22` 改为 `443` 即可

## 操作
编辑 `~/.ssh/config` 文件（没有就新增），windows在用户目录下的`.ssh`目录，添加如下内容
```shell
Host github.com
    HostName ssh.github.com
    User git
    Port 443
```

## 验证
```shell
ssh -T git@github.com
```
