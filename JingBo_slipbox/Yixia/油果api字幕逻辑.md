* Comment
	* Date : [[2021-01-12_Tue]] 
	* Sources : [[测试对接 服务&产品#油果api]]
		
	
	



# 油果api字幕逻辑
-	视频有字幕文件
		
		判断，是否出字幕
		
		
-	不出字幕，逻辑1，没压中文 及 中文账号或音乐或舞蹈 及 非用户上传字幕
		
		(rmdLable <> 70 and tagging <> 3) & (areaType = 1 or topCategory in (19,23)) & captions not in (zh,en)
		
		
-	不出字幕，逻辑2，压中文 及 任意
		
		(rmdLable = 70 or tagging = 3) & (areaType = * or topCategory = *) 
		
		
-	出字幕，逻辑1，没压中文 及 中文账号或音乐或舞蹈 及 用户上传字幕，用户上传中文>用户上传英文
		
		(rmdLable <> 70 and tagging <> 3) & (areaType = 1 or topCategory in (19,23)) & captions in (zh,en) default zh>en
		
		
-	出字幕，逻辑2，没压中文 及 非中文账号或非音乐或非舞蹈，中文>英文 按翻译质量排序
		
		(rmdLable <> 70 and tagging <> 3) & (areaType <> 1 or topCategory not in (19,23)) , default zh>zh-Trans>zh-Trans-auto> en(primitive=1)> en(primitive=2)