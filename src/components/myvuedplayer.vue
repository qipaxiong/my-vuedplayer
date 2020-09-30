<!--
 * @Description:
 * @Version: 0.1
 * @Autor: 黄鹏举
 * @Date: 2020-09-26 23:23:54
 * @LastEditors: Seven
 * @LastEditTime: 2020-09-29 23:36:34
-->
<template>
<div class="dplayer" ref="dplayer">
</div>
</template>
<script>
import DPlayer from 'dplayer'
export default {
  name: 'myvuedplayer',
  props: {
    options: {
      type: Object
    }
  },
  data () {
    return {
      dp: null
    }
  },
  mounted () {
    this.options.container = document.querySelector('.dplayer')
    this.dp = new DPlayer(this.options)
  },
  methods: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
