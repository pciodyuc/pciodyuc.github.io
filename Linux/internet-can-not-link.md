### 网络已禁用

```
sudo service network-manager stop
sudo rm /var/lib/NetworkManager/NetworkManager.state
sudo service network-manager start
```

在这之前还做了一个操作，当时没有起作用，不知道到底有没有关系

```shell
sudo /etc/NetworkManager/NetworkManager.conf
# 将managed=false改成true，重启一下就可以了。
```



