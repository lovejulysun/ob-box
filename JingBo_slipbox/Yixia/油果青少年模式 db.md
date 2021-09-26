* Comment
	* Date : [[2021-01-19_Tue]] 
	* Sources : [[测试对接 服务&产品#油果api]]
		


# 油果青少年模式 db/redis
> 当前 客户端提交 忘记密码 申诉，发企业微信群消息，包含 uid + 申诉 照片
> 手动 修改 db/redis 状态
	
## mysql
测试环境
```
mysql://kuaigeng_root:1Hlr0Dmu1RAfSX3F@rm-2zejzf7h4vqrp3546.mysql.rds.aliyuncs.com/service_user
```

Tables: user_younger

## redis key
测试环境

```
# redis-cli -h 10.0.12.126 -p 6380 -a Xagy4daBPcPAYTl3
> get u:younger:110:630789311811419227  
"\\n\\x12630789311811419227\\x10n\\x1a\\x044321 \\x01"

```
Key  = "u:younger:%d:%s"  //青少年信息缓存，string 类型，go语言序列化后存储