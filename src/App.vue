<!--
 * @Description:
 * @Version: 0.1
 * @Autor: 黄鹏举
 * @Date: 2020-09-26 23:23:54
 * @LastEditors: Seven
 * @LastEditTime: 2020-10-01 00:32:37
-->
<template>
  <div id="app">
    <myvueaplayer :options="options" ref="aplayer"></myvueaplayer>
  </div>
</template>

<script>
import myvueaplayer from "./components/myvueaplayer.vue";

export default {
  name: "App",
  components: {
    myvueaplayer,
  },
  data() {
    return {
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
      ap: null,
    };
  },
  mounted() {
    this.ap = this.$refs.aplayer.ap;
    //https://api.fczbl.vip/163/?type=playlist&id=2003373695
  },
  methods: {},
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
