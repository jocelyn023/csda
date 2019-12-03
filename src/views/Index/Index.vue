<template>
  <div class="index">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <GlobalFooter />
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue';
import GlobalFooter from '@/components/GlobalFooter/GlobalFooter.vue';

@Component({
  components: {
    HelloWorld,
    GlobalFooter,
  },
})
export default class Index extends Vue {
  // @Prop() private active!: string;
}
</script>