<template>
  <div
    class="bg-green-50 shadow-lg rounded-lg overflow-hidden p-3 m-4 border-1 border-green-800 hover:border-amber-700 hover:bg-amber-50 relative"
  >
    <div class="py-2 text-xl text-green-800 font-medium">{{ title }}</div>
    <div class="mb-1 text-sm">
      <span class="text-2xl pr-1 font-medium">{{ value }}K</span>
      <span
        :class="percentage >= 0 ? 'bg-green-300' : 'bg-red-200'"
        class="rounded-2xl text-sm px-2"
        >{{ percentage }}%</span
      >
      Vs last month
    </div>
    <div class="absolute top-8 right-5">
      <i :class="icon" class="text-3xl"></i>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Card',
  props: {
    title: {
      type: String,
      default: 'Unique Visitors',
    },
    value: {
      type: String,
      default: '24.7',
    },
    percentage: {
      type: Number,
      default: 20,
    },
    icon: {
      type: String,
      default: 'fa-solid fa-check-circle',
    },
  },
}
</script>
