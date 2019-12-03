<template>
  <div class="globalFooter">
    <van-tabbar v-model="active">
      <van-tabbar-item name="home" icon="home-o">首页</van-tabbar-item>
      <van-tabbar-item name="me" icon="search" info="5">我的</van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import { Tabbar, TabbarItem } from 'vant';

@Component({
  components: {
    [Tabbar.name]: Tabbar,
    [TabbarItem.name]: TabbarItem,
  }
})

export default class GlobalFooter extends Vue {
  @Prop() private active!: string;
}

</script>

<style lang="scss" scoped>
.table-operator {
  margin-bottom: 18px;

  button {
    margin-right: 8px;
  }
}
.apply-resolve{
  color:#52c41a
}
.apply-reject{
  color:#f5222d

}
</style>