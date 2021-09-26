* Metadata
	*  Sources : 
		 https://www.runoob.com/linux/linux-comm-xargs.html
	
	* Date : [[2021-01-11_Mon]] 
	* Tags : #摘抄 #Linux


## xargs -n

### 参数：
- -n num 后面加次数，表示命令在执行的时候一次用的argument的个数，默认是用所有的。


### 实例：
xargs 用作替换工具，读取输入数据重新格式化后输出。

定义一个测试文件，内有多行文本数据：
```
# cat test.txt a b c d e f g
h i j k l m n
o p q
r s t
u v w x y z
```

多行输入单行输出：
```
# cat test.txt | xargs a b c d e f g h i j k l m n o p q r s t u v w x y z
```

-n 选项多行输出：
```
# cat test.txt | xargs -n3 a b c
d e f
g h i
j k l
m n o
p q r
s t u
v w x
y z
```

