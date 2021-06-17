<template>
  <v-app id="app">
    <TheLayout>
        <router-view/>
    </TheLayout>
  </v-app>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import TheLayout from './layout/general/TheLayout.vue';

@Component({
  name: 'App',
  components: {
    TheLayout
  }
})
export default class App extends Vue {
}
</script>
<style scoped>

</style>