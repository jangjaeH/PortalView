<template>
<div>
    <v-app-bar 
     style="z-index:10;"
     color="depp-purple accent-4"
     dense
     dark
     fixed
     >
      <v-app-bar-nav-icon @click="$emit('toggleMenu')"></v-app-bar-nav-icon>

      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>       
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
</div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
@Component({
  name: 'Topbar',
  components: {
    
  }
})
export default class Topbar extends Vue {
}
</script>
<style scoped>

</style>