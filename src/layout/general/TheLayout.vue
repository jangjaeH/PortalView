<template>
    <div>
        <component :is = "layout">
             <TopBar @toggleMenu= "toggleMenu"></TopBar>
             <LeftBar :show="show"></LeftBar>
             <FooTerBar></FooTerBar>
        </component>
    </div>
</template>

<script lang="ts">
import { Vue, Component,Prop } from 'vue-property-decorator';
import { computed } from '@vue/composition-api';
import LeftBar from './component/left-bar.vue';
import TopBar from './component/top-bar.vue';
import FooTerBar from './component/footer-bar.vue'
@Component({
  name: 'TheLayout',
  components: {
      LeftBar,
      TopBar,
      FooTerBar
  },
})
export default class TheLayout extends Vue {
    @Prop () private root!: string;
    
    setup(props, {root}) {
        const layout =  computed(() => root.$router.meta.layout || 'defaultLayout');

        return {
            layout,
        }
    }
    
    private show = true;

    private toggleMenu() {
        this.show = !this.show
    }
}
</script>
<style scoped>

</style>