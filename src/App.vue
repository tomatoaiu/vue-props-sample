<template>
  <div id="app">
    <ChildComponent v-bind="propsForChild"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ChildComponent from './components/ChildComponent.vue';

@Component({
  components: {
    ChildComponent,
  },
})
export default class App extends Vue {
  propsForChild = {
    from: 'Parent',
    to: 'Child',
  }
}
</script>
