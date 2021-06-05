<template>
    <div>
        <v-divider/>
        <v-list
            nav
            dense
            subheader
        >
            <v-subheader>리스트</v-subheader>
        </v-list>
    </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
@Component({
  name: 'Leftbar',
  components: {
    
  }
})
export default class Leftbar extends Vue {
}
</script>
