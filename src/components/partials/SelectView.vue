<template>
  <section class="p-4 bg-gray-800 flex items-center justify-center h-screen">
    <div>
      <h2 class="text-white mr-4">Select</h2>
      <select class="p-2 rounded">
        <option v-for="option in selectOptions" :key="option.id" :value="option.id">
          {{ option.name }}
        </option>
      </select>
    </div>
    <div>
      <h2 class="text-white mr-4">Select</h2>
      <select class="p-2 rounded">
        <option v-for="option in selectOptions" :key="option.id" :value="option.id">
          {{ option.name }}
        </option>
      </select>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SelectView',
  data() {
    return {
      selectOptions: [
        { id: 1, name: 'Option 1' },
        { id: 2, name: 'Option 2' },
        { id: 3, name: 'Option 3' },
        { id: 4, name: 'Option 4' },
        { id: 5, name: 'Option 5' },
        { id: 6, name: 'Option 6' },
        { id: 7, name: 'Option 7' },
        { id: 8, name: 'Option 8' },
        { id: 9, name: 'Option 9' },
        { id: 10, name: 'Option 10' },
      ],
    }
  },
}
</script>

<style scoped>
/* Add any custom styles here */
</style>
