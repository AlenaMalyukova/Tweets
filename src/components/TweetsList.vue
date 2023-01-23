<template>
  <ul class="tweets-wrapper">
    <Item v-for="item in items" :key="item.id" :item="item"/>
  </ul>
</template>

<script>
import Item from '@/components/Item.vue'

export default {
  name: 'TweetsList',
  components: {
    Item
  },
  props: {
    items: {
      type: Array,
      reqired: true
    }
  },
  
}
</script>