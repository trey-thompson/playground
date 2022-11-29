<template>
  <div>
    <h2>This is Component B</h2>
    <p>inputD reads: {{bInputD}}</p>
    <hr>
    <c-component v-on:get-b-from-d="sendDToA($event)"/>
  </div>
</template>

<script>
import CComponent from './CComponent.vue'
export default {
  name: 'b-component',
  data() {
    return {
      bInputD: ""
    }
  },
  components: { CComponent },
  methods: {
    sendDToA(event) {
      console.log(event);
      this.bInputD = event;
      this.$emit('get-a-from-d',this.bInputD);
    }
  }
}
</script>

<style>

</style>