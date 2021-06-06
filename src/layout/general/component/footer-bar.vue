<template> 
  <v-footer 
    height="auto"
    color="primary lighten-1"
  >
    <v-layout
      justify-center
      row
      wrap
    >
      <v-col
        class="text-center"
        cols="12"
      >
        {{ new Date().getFullYear() }} - <strong>개발중</strong>
      </v-col>
    </v-layout>
  </v-footer>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
@Component({
  name: 'FooTerBar',
  components: {
    
  }
})
export default class FooTerBar extends Vue {
}
</script>
<style scoped>

</style>
