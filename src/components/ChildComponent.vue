<template>
  <p>{{ from }} {{ to }}</p>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class ChildComponent extends Vue {
  @Prop() private from!: string;

  @Prop() private to!: string;
}
</script>
