# zsh
## ls：列出文件
```ls -a``` 给出当前目录下所有文件，包括“隐藏”文件(a=all)

```ls a*``` 列出当前目录下以字母a开头的所有文件

```ls -l``` 可以查看各文件权限

```ls -al``` 上面两个连起来
## cd：切换到指定目录
```cd ~``` 切换到主目录

```cd /123``` 切换到目录/123

```cd root``` 切换到当前目录下的root目录

```cd /``` 切换到根目录

```cd ..``` 切换到到上一级目录

```cd ../..``` 切换到上二级目录
## mkdir：创建一个目录
```mkdir 123``` 建立一个名为123的目录
## touch：创建文件
```touch 123.txt``` 创建一个名为123的txt文件
## grep：搜索文件
```例:grep bible /etc/exports (表示在文件exports中查找包含bible的所有类)```

```
常用参数
-c 计算找到 ‘搜寻字符串’(即 pattern) 的次数
-i忽略大小写的不同，所以大小写视为相同
-n 输出行号
-v 反向选择，打印不匹配的行
-r 递归搜索
--color=auto 将找到的关键词部分加上颜色显示
```
## vim：编辑文件
```进入后 i 进入编辑插入模式```

```ESC退出编辑模式```

```:wq是保存，q是退出(切记加冒号！！！)```
## mv：移动和重命名文件
```mv a b``` 将a文件重命名为b

```mv a /root``` 把当前目录下的a文件移动到/tmp/目录下

```mv ./123 ../``` 将当前目录下的123文件移动到上一层目录
## rm：删除文件和目录
```rm a``` 删除文件a

```rm *``` 删除当前目录下的所有文件（未隐藏文件）。rm命令不删除目录，除非也指定了-r(递归)参数。

```rm -rf .git``` 强制删除git(可以删除隐藏文件)目录以及其所有内容
## chmod——更改文件权限
```”drwxrwxrwx“=4+2+1 4+2+1 4+2+1=777```

```读、写、运行三项权限可以用数字表示，r=4,w=2,x=1```

```777就是rwxrwxrwx，意思是该登录用户（可以用命令id查看）、他所在的组和其他人都有这个文件的最高权限```

```chmod 777 123.md这个命令表示给123这个md文件最高权限```
# [ssh](https://docs.github.com/cn/github/authenticating-to-github)
## 检查ssh密钥
```ls -al ~/.ssh```
## 生成ssh密钥
```ssh-keygen -t ed25519 -C "your_email@example.com"```
## 将 SSH 密钥添加到 ssh-agent
```ssh-add ~/.ssh/id_ed25519```
## 将 SSH 密钥添加到github
```将.ssh/id_ed25519.pub内容复制到github-settings-ssh and gpg keys-news ssh key```
