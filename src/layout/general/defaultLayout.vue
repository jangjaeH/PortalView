<template>
    <div>
        <TopBar></TopBar>
        <LeftBar></LeftBar>
        <slot/>
        <FooterBar></FooterBar>
    </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import LeftBar from './component/left-bar.vue';
import TopBar from './component/top-bar.vue';
import FooTerBar from './component/footer-bar.vue'
@Component({
  name: 'defaultLayout',
  components: {
      LeftBar,
      TopBar,
      FooTerBar
  },
})
</script>