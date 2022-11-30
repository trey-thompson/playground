<template>
  <div>
    <h2>This is Component D</h2>
    <p> inputD reads: {{inputD}} </p>
    <input type="text"
      v-model.lazy.trim="inputD"
      v-on:change="sendDToC($event.target.value)"
    >
  </div>
</template>

<script>
export default {
  name: 'd-component',
  props: {

  },
  data() {
    return {
      inputD: ""
    }
  },
  methods: {
    sendDToC(event) {
      console.log(event);
      this.$emit('get-c-from-d',event);
    }
  }

}
</script>

<style>

</style>