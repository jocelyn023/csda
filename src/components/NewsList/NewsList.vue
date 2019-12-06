<template>
  <div class="newsList">
    <van-tabs type="card" color="#b30101" title-inactive-color = "#333">
      <van-tab v-for="index in 8" :title="'标签 ' + index" :key='index'>
        内容 {{ index }}
        <NewsCard :id="index" />
      </van-tab>
    </van-tabs>
  </div>
</template>

<script lang="ts"> 
  import { Vue , Component, Prop } from 'vue-property-decorator'
  import NewsCard from '@/components/NewsCard/NewsCard.vue'

  @Component({
    components: {
      NewsCard
    }
  })

  export default class NewsList extends Vue {

  }

</script>

<style lang="scss">
  .newsList .van-tabs--card .van-tabs__nav--card .van-tab {
    border-right: none;
  }
  .newsList .van-tabs--card > .van-tabs__wrap {
    height: 44px
  }
  .newsList .van-tabs__nav--card {
    margin: 0;
    height: 44px;
    line-height: 44px;
    border: none;
  }
  .newsList .van-tabs__nav--card .van-tab {
    line-height: 44px;
  }
</style>
