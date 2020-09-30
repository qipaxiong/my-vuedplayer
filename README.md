<!--
 * @Description: 
 * @Version: 0.1
 * @Autor: 黄鹏举
 * @Date: 2020-09-26 23:24:10
 * @LastEditors: Seven
 * @LastEditTime: 2020-10-01 00:41:52
-->
# my-vuedplayer
一个vue 的 的 aplayer插件
## Project setup
```bash
npm install my-vueaplayer --save
```
import my-vueaplayer from "my-vueaplayer";

export default {
  components: {
    myvueaplayer,
  }
}
## props
## 详情地址请参考 https://aplayer.js.org/#/zh-Hans/?id=参数
## 参数(options)
 options: {
        fixed: true,
        mini: false,
        autoplay: false,
        theme: "#FADFA3",
        loop: "all",
        order: "random",
        preload: "auto",
        volume: 0.7,
        mutex: true,
        listFolded: false,
        listMaxHeight: 90,
        lrcType: 3,
        audio: [
          {
            name: "name1",
            artist: "artist1",
            url: "url1.mp3",
            cover: "cover1.jpg",
            lrc: "lrc1.lrc",
            theme: "#ebd0c2",
          },
          {
            name: "name2",
            artist: "artist2",
            url: "url2.mp3",
            cover: "cover2.jpg",
            lrc: "lrc2.lrc",
            theme: "#46718b",
          },
        ],
      },
## 参数(options)
名称	默认值	描述
## 参数(options)
container	document.querySelector('.aplayer')	播放器容器元素
## 参数(options)
fixed	false	开启吸底模式, 详情
## 参数(options)
mini	false	开启迷你模式, 详情
## 参数(options)
autoplay	false	音频自动播放
## 参数(options)
theme	'#b7daff'	主题色
## 参数(options)
loop	'all'	音频循环播放, 可选值: 'all', 'one', 'none'
## 参数(options)
order	'list'	音频循环顺序, 可选值: 'list', 'random'
## 参数(options)
preload	'auto'	预加载，可选值: 'none', 'metadata', 'auto'
## 参数(options)
volume	0.7	默认音量，请注意播放器会记忆用户设置，用户手动设置音量后默认音量即失效
## 参数(options)
audio	-	音频信息, 应该是一个对象或对象数组
## 参数(options)
audio.name	-	音频名称
## 参数(options)
audio.artist	-	音频艺术家
## 参数(options)
audio.url	-	音频链接
## 参数(options)
audio.cover	-	音频封面
## 参数(options)
audio.lrc	-	详情
## 参数(options)
audio.theme	-	切换到此音频时的主题色，比上面的 theme 优先级高
## 参数(options)
audio.type	'auto'	可选值: 'auto', 'hls', 'normal' 或其他自定义类型, 详情
## 参数(options)
customAudioType	-	自定义类型，详情
## 参数(options)
mutex	true	互斥，阻止多个播放器同时播放，当前播放器播放时暂停其他播放器
## 参数(options)
lrcType	0	详情
## 参数(options)
listFolded	false	列表默认折叠
## 参数(options)
listMaxHeight	-	列表最大高度
## 参数(options)
storageName	'aplayer-setting'	存储播放器设置的 localStorage key