# linux使用好帮手

1. zsh and oh-my-zsh

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

   

