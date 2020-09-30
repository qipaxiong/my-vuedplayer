<!--
 * @Description: 
 * @Version: 0.1
 * @Autor: 黄鹏举
 * @Date: 2020-09-26 23:24:10
 * @LastEditors: Seven
 * @LastEditTime: 2020-10-01 01:03:21
-->
# my-vuedplayer
一个vue 的 的player插件
## Project setup
```bash
npm install my-vuedplayer --save
```
import myvuedplayer from "my-vuedplayer";

export default {
  components: {
    myvuedplayer,
  }
}
## dplayer 详情地址

http://dplayer.js.org/zh/

## dplayer 基本参数

参数(options)
## dplayer
DPlayer 有丰富的参数可以自定义你的播放器实例
## dplayer
名称	默认值	描述
## dplayer
container	document.querySelector('.dplayer')	播放器容器元素
## dplayer
live	false	开启直播模式, 见#直播
## dplayer
autoplay	false	视频自动播放
## dplayer
theme	'#b7daff'	主题色
## dplayer
loop	false	视频循环播放
## dplayer
lang	navigator.language.toLowerCase()	可选值: 'en', 'zh-cn', 'zh-tw'
## dplayer
screenshot	false	开启截图，如果开启，视频和视频封面需要允许跨域
## dplayer
hotkey	true	开启热键，支持快进、快退、音量控制、播放暂停
## dplayer
airplay	true	在 Safari 中开启 AirPlay
## dplayer
preload	'auto'	视频预加载，可选值: 'none', 'metadata', 'auto'
## dplayer
volume	0.7	默认音量，请注意播放器会记忆用户设置，用户手动设置音量后默认音量即失效
## dplayer
playbackSpeed	[0.5, 0.75, 1, 1.25, 1.5, 2]	可选的播放速率，可以设置成自定义的数组
## dplayer
logo	-	在左上角展示一个 logo，你可以通过 CSS 调整它的大小和位置
## dplayer
apiBackend	-	自定义获取和发送弹幕行为，见#直播
## dplayer
video	-	视频信息
## dplayer
video.quality	-	见#清晰度切换
## dplayer
video.defaultQuality	-	见#清晰度切换
## dplayer
video.url	-	视频链接
## dplayer
video.pic	-	视频封面
## dplayer
video.thumbnails	-	视频缩略图，可以使用 DPlayer-thumbnails 生成
## dplayer
video.type	'auto'	可选值: 'auto', 'hls', 'flv', 'dash', 'webtorrent', 'normal' 或其他自定义类型, 见#MSE 支持
## dplayer
video.customType	-	自定义类型, 见#MSE 支持
## dplayer
subtitle	-	外挂字幕
## dplayer
subtitle.url	required	字幕链接
## dplayer
subtitle.type	'webvtt'	字幕类型，可选值: 'webvtt', 'ass'，目前只支持 webvtt
## dplayer
subtitle.fontSize	'20px'	字幕字号
## dplayer
subtitle.bottom	'40px'	字幕距离播放器底部的距离，取值形如: '10px' '10%'
## dplayer
subtitle.color	'#fff'	字幕颜色
## dplayer
danmaku	-	显示弹幕
## dplayer
danmaku.id	required	弹幕池 id，必须唯一
## dplayer
danmaku.api	required	见#弹幕接口
## dplayer
danmaku.token	-	弹幕后端验证 token
## dplayer
danmaku.maximum	-	弹幕最大数量
## dplayer
danmaku.addition	-	额外外挂弹幕，见#bilibili 弹幕
## dplayer
danmaku.user	'DIYgod'	弹幕用户名
## dplayer
danmaku.bottom	-	弹幕距离播放器底部的距离，防止遮挡字幕，取值形如: '10px' '10%'
## dplayer
danmaku.unlimited	false	海量弹幕模式，即使重叠也展示全部弹幕，请注意播放器会记忆用户设置，用户手动设置后即失效
## dplayer
contextmenu	[]	自定义右键菜单
## dplayer
highlight	[]	自定义进度条提示点
## dplayer
mutex	true	互斥，阻止多个播放器同时播放，当前播放器播放时暂停其他播放器