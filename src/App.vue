<template>
  <div id="app">
    <Thelayout>

    </Thelayout>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import Thelayout from './layout/general/TheLayout.vue';

@Component({
  name: 'App',
  components: {
    Thelayout
  }
})
export default class App extends Vue {
}
</script>
