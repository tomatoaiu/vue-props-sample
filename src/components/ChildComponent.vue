<template>
  <p>{{ from }} {{ to }}</p>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

type PorpsForChild = {
  from: string,
  to: string
}

@Component
export default class ChildComponent extends Vue {
  @Prop({ type: Object, required: true }) private porpsForChild!: PorpsForChild;

  get from() {
    return this.porpsForChild.from;
  }

  get to() {
    return this.porpsForChild.to;
  }
}
</script>
