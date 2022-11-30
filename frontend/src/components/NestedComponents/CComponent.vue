<template>
  <div>
    <h2>This is Component C</h2>
    <p>inputD reads: {{cInputD}}</p>
    <hr>
    <d-component v-on:get-c-from-d="sendDToB($event)"/>
  </div>
</template>

<script>
import DComponent from './DComponent.vue'
export default {
  name: 'c-component',
  data() {
    return {
      cInputD: ""
    }
  },
  components: { DComponent },
  methods: {
    sendDToB(event) {
      console.log(event);
      this.cInputD = event;
      this.$emit('get-b-from-d',this.cInputD);
    }
  }

}
</script>

<style>

</style>