### 本地git和github关联（win）

1. 假定已有github账号

2. 本地配置用户名和邮箱

   ```shell
   git config --global user.name ”yourusername”
   git config--global user.email ”youremail”
   cat ~/.gitconfig
   ```

3. 通过命令 git init 把当前目录变成git可以管理的仓库

   ```shell
   git init
   ```

4. 生成SSH Key

   ```shell
   ssh-keygen -t rsa -C"你的邮箱"
   # 用户主目录/.ssh/下有两个文件，id_rsa是私钥，id_rsa.pub是公钥
   ```

5. 登录GitHub，打开"SSH Keys"页面

   key 处填粘贴id_rsa.pub文件的内容

6. 测试ssh key是否成功

   ```shell
   ssh -T git@github.com
   ```

### 远程库与本地库之间的操作

1. 远程库-->本地库

```shell
git clone git@github.com:***/***.git
```

2. 获取用

   ```shell
   git pull origin master
   ```

3. 推送master分支的所有内容 

   ```shell
   git add .
   git commit -m "new file"
   git push .
   # git push -u origin master
   ```

   