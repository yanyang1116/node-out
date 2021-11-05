<template>
  <div><slot /></div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class NodeOutTransition extends Vue {
  @Prop() private source!: [];
  private beforeUpdate(value: any, oldValue: any) {
    console.log(value, oldValue, 7689087);
  }
  // @Prop({ type: String, default: "" }) private msg!: string;
}
</script>

<style scoped></style>
