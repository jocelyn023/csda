<template>
  <div id="app">
    <div v-show="!(path==='/about')">
      <GlobalFooter />
    </div>
    
    <router-view />
  </div>
</template>

<script lang="ts">
import { Component, Vue, Watch } from 'vue-property-decorator'
import GlobalFooter from '@/components/GlobalFooter/GlobalFooter.vue';

@Component({
  components: {
    GlobalFooter
  }
})


export default class App extends Vue {
  private headerShow:boolean = true;
  private path:string  = '';

  @Watch('$route')
    routechange(to: any, from: any) {
      this.path = to.path;
    }

  private mounted() {
    this.path = this['$route'].path;
  }
  
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
