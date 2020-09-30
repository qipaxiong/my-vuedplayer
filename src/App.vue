<!--
 * @Description:
 * @Version: 0.1
 * @Autor: 黄鹏举
 * @Date: 2020-09-26 23:23:54
 * @LastEditors: Seven
 * @LastEditTime: 2020-09-29 23:18:56
-->
<template>
  <div id="app">
    <button class="btn btn-primary" @click="switchHandle">switch</button>
    <myvuedplayer
      style="width: 500px; margin: 0 auto"
      :options="options"
      @play="play"
      ref="dplayer"
    ></myvuedplayer>
  </div>
</template>

<script>
import myvuedplayer from "./components/myvuedplayer.vue";

export default {
  name: "App",
  components: {
    myvuedplayer,
  },
  data() {
    return {
      options: {
        video: {
          url: "http://static.smartisanos.cn/common/video/t1-ui.mp4",
          pic:
            "http://static.smartisanos.cn/pr/img/video/video_03_cc87ce5bdb.jpg",
        },
        autoplay: false, //视频自动播放
        screenshot: true, //开启截图，如果开启，视频和视频封面需要允许跨域
        live: false, //开启直播模式
        loop: false, //视频循环播放
        theme: "#f40", //主题色
        preload: "auto", //视频预加载，可选值: 'none', 'metadata', 'auto'
        hotkey: true, //开启热键，支持快进、快退、音量控制、播放暂停
        airplay: false, //在 Safari 中开启 AirPlay
        danmaku: true,
        danmaku: {
          id: "9E2E3368B56CDBB4",
          api: "https://api.prprpr.me/dplayer/",
          token: "tokendemo",
          maximum: 1000,
          addition: ["https://api.prprpr.me/dplayer/v3/bilibili?aid=21322"],
          user: "DIYgod",
          bottom: "15%",
          unlimited: true,
        },
        contextmenu: [
          {
            text: "GitHub",
            link: "https://github.com/MoePlayer/vue-dplayer",
          },
        ],
      },
      dp: null,
    };
  },
  mounted() {
    this.dp = this.$refs.dplayer.dp;
  },
  methods: {
    play() {
      console.log("play callback");
    },
    switchHandle() {
      this.dp.switchVideo({
        url: "http://static.smartisanos.cn/common/video/video-jgpro.mp4",
      });
      this.dp.play();
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
