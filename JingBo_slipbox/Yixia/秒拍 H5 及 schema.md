* Comment
	* Date : [[2021-01-11_Mon]] 
	* Sources : [[测试对接 服务&产品#秒拍 H5]]
		
	


# 秒拍 H5 及 schema

 ios v7.4.1
 安卓 v7.2.84
 
1. 视频详情页
https://n.miaopai.com/media/0LrO097byJxlxev14zRuUM-d9RsTouXY.htm

2. 用户主页
https://n.miaopai.com/personal/xGj28B56otkjf2R8fr36pQ__.htm

3. 话题
https://n.miaopai.com/topic/r69rQtiRPzSjabESCXKfgg__.htm

scheme:
```
//视频详情页
 {
        ios: `miaopai://detail?smid=${id}`,
        android: `miaopai://square.app/start?type=0&smid=${id}`
}
//首页
 {
            ios: 'miaopai://',
            android: 'miaopai://square.app/start'
}
//个人页（/personal/:suid）
 {
          ios: 'miaopai://profile?suid=' + id,
          android: 'miaopai://square.app/start?type=1&suid=' + id
 }
//悬赏页（/reward/:srwid）
 {
            ios: `miaopai://reward?srwid=${id}`,
            android: `miaopai://square.app/start?type=26&rewardId=${id}`
 }
//话题页（/topic/:stid）
 {
            ios: `miaopai://topics?stid=${id}`,
            android: `miaopai://square.app/start?type=8&topicid=${id}`
          }
//参与话题
{
            ios: `miaopai://capture?topic=${id}`,
            android: `miaopai://square.app/start?type=3&topic=${id}`
          }

{
            ios: `miaopai://detail?smid=${id}`,
            android: `miaopai://square.app/start?type=3&scid=${id}`
          }
//粉丝打卡
 {
        ios: `miaopai://`,
        android: `miaopai://square.app/starts`
      }
//刷新页面
openlink = {
          ios: `miaopai://browsermp?url=${window.location.href}`,
          android: `miaopai://square.app/start?type=38&url=${window.location.href}`
        }
//星拜年
let openlink = {
        ios: `miaopai://showcapturemenu?isShowFace=true`,
        android: `miaopai://square.app/start?type=3&isShowFace=true`
      }
```