---
title: Linux命令基础


---



# Linux命令基础

‍

### pwd 命令（打印当前工作路径）

```
~  当前用户家目录的缩写（/home/ubuntu）
.  当前目录
.. 上一级目录
/  根目录
```

### cd 切换工作路径

```
cd /    //切换到根目录
cd      //切换到家目录
cd~     //同上
cd ..   //切换到上一级
cd ../../A/B    //切换到上一级的上一级的A里面的B
cd /home/A/B    //绝对路径
cd -     //返回到上一次路径
```

### ls 列举当前目录下内容

```
ls -l  //列举当前目录下详细内容
ls -a  //列举当前目录所有内容（包括隐藏文件）
ls -a-l
```

​![image](assets/image-20240213163141-krb8bi5.png)​

rwx 可读可写可执行

### find 查找

```
find -name ABC  //在当前目录查找名字为ABC的文件
locate  ABC     //全局搜索ABC
```

Ctrl + T 清屏

### cat 打印输出文件内容

```
cat ABC
```

### head 查看某个文件头部

```c
head stdio.h   //默认查看前十行
head -20 stdio.h  //查看前20行
```

### tail 查看文件尾部（与 head 相反）

‍

### grep 在文件中查找指定内容

```
grep printf stdio.h -n   
//在stdio.h中查找printf并且输出带有行号的内容
```

### chmod 修改文件权限

```
chmod 763 ABC   //修改ABC文件权限rwx
拥有者可读可写可执行
同组用户可读可写
其他用户可写可执行
```

### cp 复制文件

```
cp ABC BCD   //把ABC复制成BCD
cp abc/  bcd  //复制目录文件abc变成bcd，后面加 -r递归复制，复制目录文件里面内容
```

### mv 移动文件/重命名

```
mv ABC abc   //移动ABC到abc目录里
mv abc/ 123  //把abc重命名为123
```

### mkdir 创建目录文件

```
mkdir abc //创建目录名为abc
```

### touch 创建普通文件

```
touch abc.c  //创建一个普通文件abc.c
```

### rm 删除文件

```
rm abc.c  //删除普通文件
rm abc -r  //递归删除目录文件abc
```

### sudo 临时使用超级用户权限

```
sudo touch abc.c  //临时使用超级用户权限创建普通文件
sudo -s //临时切换为超级用户
exit 退出

```

### man 手册

```
man man   //查看man手册是什么
man -f mkfifo  //查看mkfifo出现在哪一本手册
man 1 mkfifo  //在第一本手册中查看mkfifo的解析
```

‍
