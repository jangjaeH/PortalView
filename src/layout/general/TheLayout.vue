<template>
    <div>
        <leftbar></leftbar>
    </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import leftbar from './component/left-bar.vue';
@Component({
  name: 'TheLayout',
  components: {
      leftbar
  }
})
export default class TheLayout extends Vue {
}
</script>
