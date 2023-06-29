<template>
      <p>
    <data-item
      v-for="item in records"
      :key="item.id"
      :title="item.title"
      :quotes="item.quote"
      :image="item.image"
    ></data-item>
  </p>
</template>

<script>
import DataItem from './DataItem.vue'

export default {
    components: { DataItem },
    props: ['records']
}
</script>

<style scoped>
p {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>