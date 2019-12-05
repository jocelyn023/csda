<template>
  <div>
    <van-tabbar route>
      <van-tabbar-item 
        replace
        to="/home"
        icon="home-o">
        首页
      </van-tabbar-item>
      <van-tabbar-item 
        replace
        to="/about"
        icon="home-o"
      >
        我的
      </van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script lang="ts"> 
  import { Vue , Component } from 'vue-property-decorator'

  @Component
  export default class GlobalFooter extends Vue{


  }

</script>

<style lang="scss">

</style>
