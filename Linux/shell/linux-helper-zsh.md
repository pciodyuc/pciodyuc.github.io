# linux使用好帮手-ZSH

##### 目录

* [安装 zsh and oh-my-zsh](#安装 zsh and oh-my-zsh)
* [linux 默认shell 使用zsh](#linux 默认shell 使用zsh)
* [](#)
* [](#)
* [](#)

### 安装 zsh and oh-my-zsh

```shell
apt-get install zsh
# oh-my-zsh官网 https://ohmyz.sh/#install
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
# 更换zsh主题
vim ~/.zshrc
# 修改
ZSH_THEME="af-magic"
#保存
source ~/.zshrc

```

下载时遇到问题，==The TLS connection was non-properly terminated.==

问题原因：代理设置出错；解决方案：重置代理

```shell
git config --global  --unset https.https://github.com.proxy 
git config --global  --unset http.https://github.com.proxy 
```

### linux 默认shell 使用zsh

```shell
vim ~/.bashrc
# 在.bashrc文件中添加如下
if [ -t 1 ]; then
    exec zsh
fi
# ----end-------
source ~/.bashrc
```



