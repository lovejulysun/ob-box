# ios play


## 开始播放
- [ ] mediaType 缺失
"params": {
		"event": [{
			"mediaId": "6748193979507937280",
			"source": 3,
			"eventId": "play",
			"videoId": "6748193979507937280",
			"duration": "750"
		}]
		
## 停止播放
- [ ] 多了不少 wiki 没列到的参数
"params": {
		"event": [{
			"videoViewLoadDuration2": 0,
			"pauseTimes": 1,
			"endDuration": "623",
			"loadCount": 0,
			"subscribed": 0,
			"videoId": "6748193979507937280",
			"playDuration": 750,  // 当前等于视频时长，实际累计播放时长 < 视频时长
			"loc": 0,
			"url": "http:\/\/trans-test.oss-cn-beijing.aliyuncs.com\/stream\/S0V74J8hfy-OFmqVldSQMlraAXGiG1pCrGwgow___32.mp4?ssig=08141b8fae0d96eb43c032b8e3e27e59&time_stamp=1611564338747",
			"retryTimes": 0,
			"soVersion": "",
			"mediaId": "6748193979507937280",
			"lastVideoId": "",
			"bufAllTimePreSecond": 0,
			"source": 3,
			"share": false,
			"serverIp": "",
			"socketPacket": 0,
			"favorited": false,
			"dnsResolve": 0,
			"replayTimes": 0,
			"commented": false,
			"fullscreen": false,
			"soType": "ijk",
			"videoViewLoadDuration": 0,
			"bufAllTime": 0,
			"requestUriDuration": 0,
			"socketConnect": 0,
			"eventId": "play",
			"ijkVersion": "0.8.8",
			"videoCodeType": "H264",
			"error": 0,
			"themeId": "0",
			"refreshCount": 0,
			"duration": "750",
			"Digg_bury": 0,
			"bufTime": 0,
			"uriFrom": 0,
			"watchType": 1, // 实际是在关注 feed 留观看，应为0
			"uid": "701739442852985878",
			"rom": "iphone7 plus",
			"streamPacket": 0,
			"bufTimes": 1,
			"bufTimesPreSecond": 0,
			"bufTimes2": 0,
			"decodeFrame": 0,
			"bufAllTime2": 0,
			"mediaType": 1,
			"redirectUrl": "",
			"errorExtra": "",
			"viewCommentPages": 0,
			"decodeType": "4",
			"viewCommented": false,
			"seekTimes": 0
		}]
		
		
		
- [ ] 漏报。详情页播放， 向下 滑动 至 新视频时，漏报 老视频
- [ ] watchType = 1 详情页类型没有
- [ ]  搜索页7、发现5、我的主页20，因都进入 详情页 播放，source 都报成了2
- [ ] 当为发现页 视频时， 缺失 channelId  
- [ ] 信息流card、详情页、全屏 来回切换，1、需明确是否要上报；2、上报watchType 要以 最终结束播放 时所处 位置；
- [ ] 