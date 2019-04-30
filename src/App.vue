<template>
  <div id="app">
    <ChildComponent :porps-for-child="{
      from: 'Parent',
      to: 'Child'
    }"/>
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
  porpsForChild = {
    from: 'Parent',
    to: 'Child',
  }
}
</script>
