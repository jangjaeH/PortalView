<template>
    <div>
        <TopBar></TopBar>
        <LeftBar></LeftBar>
        <FooTerBar></FooTerBar>
    </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import LeftBar from './component/left-bar.vue';
import TopBar from './component/top-bar.vue';
import FooTerBar from './component/footer-bar.vue'
@Component({
  name: 'TheLayout',
  components: {
      LeftBar,
      TopBar,
      FooTerBar
  }
})
export default class TheLayout extends Vue {
}
</script>
<style scoped>

</style>