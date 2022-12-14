---
{"dg-publish":true,"dg-permalink":"配置oh my zsh","permalink":"/配置oh my zsh/","dgPassFrontmatter":true}
---


#终端 #terminal #终端教程 #zsh #oh_my_zsh

 **终端知识点**
“～ ” 你的home目录，在OS X下位于/Users/你的用户名/
“.” 类 unix 下的隐藏文件，文件名带"."之后在 GUI 文件管理器和 ls 的默认设置下不会显示出来，使用 ls －a 命令可以显示出这些文件，下面的命令就是进入 home 目录下的隐藏文件 zshrc 文件
```
~/.zshrc
```

**设定当前文件**
source .zshrc


## 一 ：shell

判断当前shell
```
echo $SHELL
```

查看安装了哪些 shell
```
cat /etc/shells
```

设置默认 shell 为 zsh 
按**Command+Q**退出终端后重启终端，就可以使用**zsh**的终端了
```
chsh -s /bin/zsh
```

####  MAC 默认终端安装 oh my zsh 参考：[GitHub - ohmyzsh/ohmyzsh: 🙃 ](https://github.com/ohmyzsh/ohmyzsh)
```shell
curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
```

#### OH MY ZSH 更新
``` shell
omz update

```

>[! example] 更新成功如图
![](https://raw.githubusercontent.com/Rnzi/pic/main/20221018231929.png)
[效果图](https://img-blog.csdnimg.cn/20201018204053623.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTE2NzUzMzQ=,size_16,color_FFFFFF,t_70)




## 二、安装主题：在终端中输入以下命令

```javascript
vim ~/.zshrc
```

```
vim /etc/zshrc

```
vim /etc/zshrc
找到ZSH_THEME 这行，并且将后面双引号内文字改成想要套用主题风格，按下i 键进入编辑模式，双引号内改成「agnoster」，最后按下esc 键退出编辑，并输入:wq 就可以保存退出vim 编辑模式。

## 三：细节
参考资料：[MAC 终端美化教程（来个全套）_朕.的博客-CSDN博客_mac终端美化](https://blog.csdn.net/weixin_42326144/article/details/121957795)
Powerline 字体
[GitHub - powerline/fonts: Patched fonts for Powerline users.]( https://github.com/powerline/fonts )
```
# clone
git clone https://github.com/powerline/fonts.git --depth=1
# install
cd fonts
./install.sh
# clean-up a bit
cd ..
rm -rf fonts
```


#### 语法高亮插件：
[zsh-syntax-highlighting/INSTALL.md at master · zsh-users/zsh-syntax-highlighting · GitHub](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
``` shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
```

#### 配置插件 ：在终端输入以下命令
```shell
vim ~/. zshrc
```

vim /etc/zshrc 是否一样？

1、找到 plugins=(git) 这行，
2、按下 i 键进入编辑模式
3、修改成这个样子 plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
4、最后按下 esc 键退出编辑，并输入: wq (直接 q 也行) 就可以保存退出 vim 编辑模式。
PS 配置完记得设定当前文件夹