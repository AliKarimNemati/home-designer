<template>
  <TopHeader class="fixed-top"/>
  <router-view/>
</template>

<script>
import TopHeader from '@/components/TopHeader.vue'
export default {
  components: { TopHeader }
}
</script>

<style lang="scss">
@font-face {
  font-family: main-font;
  src: url('./assets/font/mediom.ttf');
}
@font-face {
  font-family: montserrat;
  src: url('./assets/font/Montserrat-Regular.ttf');
}
body {
  margin: 0;
  font-size: 16px;
  font-family: main-font;
  background: #f4f2e8;
}
.english-text{
  font-family: montserrat;
}
.des{
  color: #929191;
}
</style>
