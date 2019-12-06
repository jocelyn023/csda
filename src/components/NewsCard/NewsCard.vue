<template>
  <div class="newsCard">
    <van-list
      v-model="loading"
      :finished="finished"
      finished-text="没有更多了"
      @load="getList"
    >
      <van-cell
        v-for="item in list"
        :key="item"
        :title="item"
      />
    </van-list>
  </div>
</template>

<script lang="ts"> 
  import { Vue , Component, Prop } from 'vue-property-decorator'
  import axios from 'axios'

  @Component

  export default class NewsCard extends Vue {
    list:any =[]
    finished:boolean = false;
    loading:boolean = false

    @Prop() private id!: string;

    getList() {
      var url = "http://dev.csda.cn.com/csda/wechartOrg/queryPageTypeArticles.spv?rand%20=0.21273219698287704";
      axios({
        url: url,
        method: 'post',
        success: function (data){
          alert(data)
        }
      })
      // $.post("", {"typeId": typeId, "pageNo": pageNum, "pageSize": "10"}, function (data, status) {
      //   alert(data, status)
      // })
      this.finished = true
      alert("This is my warning message");
    }
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
