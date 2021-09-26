# 安卓 play
- [ ] videoId 缺失
- [ ] mediaId 缺失
- [ ] refreshCount 缺失
- [ ] replayTimes 缺失

	"params": {
		"event": [{
			"channelId": "56",
			"duration": 0, // 视频时长未获取到
			"endDuration": 196439, // 视频播放结束时间点，单位秒，视频长10分钟，播放到5分钟结束，值即为 300
			"mediaType": 1,
			"playDuration": 769, //  测试实际播放时长 只有几秒到十几秒
			"retryTimes": 0,
			"source": 5,
			"watchType": 1,
			"eventId": "play"
		}]
	}
	
	"params": {
		"event": [{
			"duration": 371,
			"endDuration": 0,  // 视频播放结束时间点，单位秒
			"mediaId": "6757187706184294400",
			"mediaType": 1,
			"playDuration": 1611643311, // 实际播放时长
			"refreshCount": 0,
			"replayTimes": 0,
			"retryTimes": 0,
			"source": 1,
			"videoId": "6757187706184294400",
			"watchType": 1,  // 精选信息流 应为 0 
			"eventId": "play"
		}]
	}
}