<template>
  <div class="app">
    <router-view>aa</router-view>
    <FooterGuide v-show="$route.meta.showFooter" />
  </div>
</template>

<script>
import {mapActions} from 'vuex'
import FooterGuide from "./components/FooterGuide/FooterGuide.vue";
export default {
  name: "App",
  mounted() {
     this.getAddress()
    //  console.log(this.$store.dispatch('getAddress'))
    //  this.$store.dispatch('getAddress')
  },
  methods:{
    ...mapActions(['getAddress',])//映射函数 ， 发送请求的另一种方式
  },
  components: {
    FooterGuide,
  },
  
};
</script>

<style lang='stylus' rel="stylesheet/stylus">
.app {
  width: 100%;
  height: 100%;
  background: #f5f5f5;
}
</style>