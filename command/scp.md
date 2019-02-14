# scp (secure copy)

scp是一个基于SSH协议在网络之间进行安全传输的命令。

# 语法

```scp [可选参数] file_source file_target```

# 参数说明

* _-r_: 用于传送整个文件夹
* _-P_ port: 注意是大写的P,port指定数据传输用到的端口号。

# 实例
## 从本地复制到远程
命令格式
```
scp local_file remote_username@remote_ip:remote_folder 
或者 
scp local_file remote_username@remote_ip:remote_file 
```
指定了用户名，命令执行后需要再输入密码，第1个仅指定了远程的目录，文件名字不变，第2个指定了文件名；

应用实例

复制本地文件到远程文件夹
```
scp /home/space/music/1.mp3 root@www.runoob.com:/home/root/others/music 
```

复制本地文件到远程文件(修改文件名)
```
scp /home/space/music/1.mp3 root@www.runoob.com:/home/root/others/music/001.mp3 
```

## 从远程复制到本地

应用实例

```
scp root@www.runoob.com:/home/root/others/music/1.mp3 /home/space/music 
```

# 参考
菜鸟教程[Linux scp命令](http://www.runoob.com/linux/linux-comm-scp.html)

<<linux就该这么学>>[9.2.3 远程传输命令](https://www.linuxprobe.com/chapter-09.html#923)