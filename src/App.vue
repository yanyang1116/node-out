<template>
  <div id="app">
    <!-- <NodeOutTransition v-for="(item, index) in list" :key="index">{{ -->
    <!-- <NodeOutTransition :source="list"></NodeOutTransition> -->
    <transition>
      <div v-if="ok" name="fade" leave>toggled content</div>
    </transition>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import NodeOutTransition from "./components/NodeOutTransition.vue";

@Component({
  components: { NodeOutTransition },
})
export default class App extends Vue {
  private list: any[] = [];
  private ok = true;
  private created() {
    // this.ok = false
    // this.list = [1, 2];
    setTimeout(() => {
      // this.list = [1];
      this.ok = false;
    }, 1200);
  }
}
</script>
