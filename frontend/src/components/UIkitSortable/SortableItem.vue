<template>
  <div>
    {{item.name}} | Sort Order: {{item.sortOrder}}
  </div>
</template>

<script>
export default {
  name: 'sortable-item',
  props: {
    item: Object
  }

}
</script>

<style>

</style>