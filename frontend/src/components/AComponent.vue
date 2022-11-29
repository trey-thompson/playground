<template>
  <div>
    <h2>This is Component A</h2>
    <p>inputD reads: {{aInputD}}</p>
    <hr>
    <b-component v-on:get-a-from-d="getChanges($event)"/>
  </div>
</template>

<script>
import BComponent from './BComponent.vue'
export default {
  name: 'a-component',
  data() {
    return {
      aInputD: ""
    }
  },
  components: { BComponent },
  methods: {
    getChanges(event) {
      console.log(event);
      this.aInputD = event;
    }
  }
}
</script>

<style>

</style>