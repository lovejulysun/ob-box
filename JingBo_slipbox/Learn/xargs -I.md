* Metadata
	*  Sources : 
		 https://www.runoob.com/linux/linux-comm-xargs.html
	
	* Date : [[2021-01-11_Mon]] 
	* Tags : #摘抄 #Linux


## xargs -I

### 参数：
-   -I，将xargs的每项名称，指定一个替换字符串 {}，这个字符串在 xargs 扩展时会被替换掉，当 -I 与 xargs 结合使用，每一个参数命令都会被执行一次。

### 实例
假设一个命令为 sk.sh 和一个保存参数的文件 arg.txt：
```
#!/bin/bash 
#sk.sh命令内容，打印出所有参数。 
echo $\*
```

arg.txt文件内容：

```
# cat arg.txt 
aaa
bbb
ccc
```

与管道一起使用
```
# cat arg.txt | xargs -I {} ./sk.sh -p {} -l 
-p aaa -l
-p bbb -l
-p ccc -l
```

结合 [[xargs -n|参数 -n]]， 复制所有图片文件到 /data/images 目录下：
```
ls \*.jpg | xargs \-n1 \-I {} cp {} /data/images
```