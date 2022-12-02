<template>
  <div>
    <!-- UIkit example copied & pasted below -->
    <h2>UIkit example copied & pasted below</h2>
    <ul class="uk-grid-small uk-child-width-1-2 uk-child-width-1-4@s" uk-sortable="handle: .uk-card" uk-grid>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 1</div>
      </li>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 2</div>
      </li>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 3</div>
      </li>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 4</div>
      </li>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 5</div>
      </li>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 6</div>
      </li>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 7</div>
      </li>
      <li>
        <div class="uk-card uk-card-default uk-card-body uk-text-center">Item 8</div>
      </li>
    </ul>

    <!-- Custom approach with imported components -->
    <br>
    <hr>
    <h2>Custom approach with imported components</h2>
    <div class="uk-grid-small uk-child-width-1-2 uk-child-width-1-4@s" uk-sortable="handle: .uk-card" uk-grid>
      <sortable-item
        v-for="item in sortableItems"
        v-bind:key="item.id"
        v-bind:item="item"
        class="uk-card uk-card-default uk-card-body uk-text-center"
      />
    </div>
  </div>
</template>

<script>
import SortableItem from './SortableItem.vue'
export default {
  name: 'sortable-list',
  components: { SortableItem },
  data() {
    return {
      sortableItems: [
        {
          name: 'item1',
          sortOrder: 1
        },
        {
          name: 'item2',
          sortOrder: 2
        },
        {
          name: 'item3',
          sortOrder: 3
        },
        {
          name: 'item4',
          sortOrder: 4
        },
        {
          name: 'item5',
          sortOrder: 5
        },
        {
          name: 'item6',
          sortOrder: 6
        },
        {
          name: 'item7',
          sortOrder: 7
        },
        {
          name: 'item8',
          sortOrder: 8
        },
      ]
    }
  }
}
</script>

<style>

</style>