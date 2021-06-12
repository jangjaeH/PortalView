<template> 
  <v-footer
    height="auto"
    dark
    padless
    app
  >
    <v-card
     class="flex"
     flat
     tile
    >
      <v-card-title>
        <small>COPYRIGHT (c) 2021. jhjnag. All rights reserved.</small>
        <v-spacer></v-spacer>

        <v-btn
          v-for="menu in menus"
          :key="menu.icon"
          class="mx-4"
          dark
          icon
          @click="newPage(menu.link)"
        >
          <v-icon size="24px">
              {{ menu.icons }}
          </v-icon>
        </v-btn>
      </v-card-title>
    </v-card>
  </v-footer>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
@Component({
  name: 'FooTerBar',
  components: {
    
  },
  data: () => ({
     menus: [
      {
       icons: 'mdi-facebook',
       link: 'https://www.facebook.com/profile.php?id=100008292990107'
      },
      {
        icons: 'mdi-instagram',
        link: 'https://www.instagram.com/jhjang___._.j'
      },
      {
        icons: 'mdi-github',
        link:'https://github.com/jangjaeH'
      }
     ]
  })
})
export default class FooTerBar extends Vue {
  private newPage(joinLink: string) {
    window.open(joinLink, '_blank');
  }
}
</script>
<style scoped>

</style>
