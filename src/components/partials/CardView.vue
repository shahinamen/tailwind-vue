<script>
import Card from '../component/Card.vue'
export default {
  components: {
    Card,
  },
}
</script>
<template>
  <section class="flex flex-col justify-center items-center h-auto">
    <div class="grid grid-cols-1 mt-4 mb-4 md:grid-cols-4">
      <Card
        :title="'Unique Visitors'"
        :value="24.7"
        :percentage="20"
        :icon="'fa fa-solid fa-check-circle'"
      />
      <Card :title="'Total Pageviews'" :value="29.5" :percentage="40" :icon="'fa-solid fa-star'" />
      <Card :title="'Bounce Rate'" :value="48.8" :percentage="60" :icon="'fa-solid fa-thumbs-up'" />
      <Card
        :title="'Visit Duration'"
        :value="21.4"
        :percentage="-50"
        :icon="'fa-solid fa-face-smile'"
      />
    </div>
  </section>
</template>
