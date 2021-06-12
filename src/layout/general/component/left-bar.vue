<template>
<div>
  <v-list
  style="height: calc(100vh - 106px); margin-top:46px;"
    dark 
    width="256" 
    :class="drawerStyle"
    class="menu"
  >
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="text-h6">
          메뉴리스트
        </v-list-item-title>
        <v-list-item-subtitle>
          subtext
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>
    <v-list
      dense
      nav
    >
      <v-list-item
        v-for="item in items"
        :key="item.title"
        link
      >
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-list>
</div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';
@Component({
  name: 'Leftbar',
  components: {
    
  },
  data () {
      return {
        items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'About', icon: 'mdi-help-box' },
        ],
        right: null,
      }
    }
})
export default class Leftbar extends Vue {
  @Prop () private show!: boolean

  get drawerStyle () : string{
    if(this.show){
      return '';
    } else {
      return 'hidden';
    }
  }
}
</script>
<style scoped>
  .hidden {
    margin-left: -256px;
  }

  .menu {
    transition: margin-left 300ms;
  }
</style>