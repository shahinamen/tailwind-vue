<template>
  <section class="min-h-screen bg-amber-100">
    <div class="relative bg-white shadow-md">
      <!-- Top Menu -->
      <div
        class="h-[40px] bg-amber-500 fixed top-0 left-0 w-full z-10 flex justify-center items-center"
      >
        <h1 class="text-white text-center">Top Menu</h1>
        <div class="absolute right-4 space-x-2">
          <i class="fa-solid fa-cart-shopping text-2xl"></i>
          <span class="bg-white rounded-full px-1 absolute right-1.5">0</span>
        </div>
      </div>

      <div class="flex">
        <!-- Left Drawer -->
        <div
          class="h-screen bg-blue-500 fixed top-[40px] left-0 z-10 transition-all duration-300"
          :class="showDrawer ? 'w-[300px]' : 'w-0 overflow-hidden'"
        >
          <h1 v-if="showDrawer" class="text-white p-4">Left Side Drawer</h1>
        </div>

        <!-- Right Content -->
        <div
          class="flex-1 mt-[40px] p-4 transition-all duration-300"
          :class="showDrawer ? 'ml-[300px]' : 'ml-0 w-full'"
        >
          <h1 class="text-3xl">
            <div class="flex flex-row justify-between items-center gap-1 bg-gray-800 p-1">
              <div
                class="w-full h-32 flex justify-between items-center bg-gray-500 p-2 rounded-2xl border-1 border-cyan-700"
              >
                <div>AAAA</div>
                <i class="fa fa-solid fa-check-circle text-green-600"></i>
              </div>
              <div
                class="w-full h-32 flex justify-between items-center bg-gray-500 p-2 rounded-2xl border-1 border-cyan-700"
              >
                <div>AAAA</div>
                <i class="fa fa-solid fa-check-circle text-green-600"></i>
              </div>
              <div
                class="w-full h-32 flex justify-between items-center bg-gray-500 p-2 rounded-2xl border-1 border-cyan-700"
              >
                <div>AAAA</div>
                <i class="fa fa-solid fa-check-circle text-green-600"></i>
              </div>
              <div
                class="w-full h-32 flex justify-between items-center bg-gray-500 p-2 rounded-2xl border-1 border-cyan-700"
              >
                <div>AAAA</div>
                <i class="fa fa-solid fa-check-circle text-green-600"></i>
              </div>
              <div>
                <i
                  class="fa-classic fa-solid fa-align-left fa-fw cursor-pointer"
                  @click="handleDrawer"
                ></i>
              </div>
              <div>Dashboard</div>
            </div>
            <input type="text" v-model="text" class="w-full p-2 mt-4" />
            <div>Lowercase: {{ lowerCaseText }}</div>
            <div>Uppercase: {{ upperCaseText }}</div>
            <div>
              <h2 class="text-2xl mt-4">Fruit List</h2>
              <ul>
                <!-- Iterate over the list and display each fruit -->
                <li v-for="(fruit, index) in list" :key="index">{{ index + 1 }}. {{ fruit }}</li>
              </ul>
            </div>
          </h1>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import {
  generateLowerCase,
  generateUpperCase,
  generateFruitList,
  calculationPercentage,
} from '../resources/function'

export default {
  name: 'DrawerView',
  data() {
    return {
      showDrawer: true,
      text: '', // Input text
      list: generateFruitList(),
      percent: calculationPercentage(),
    }
  },
  computed: {
    lowerCaseText() {
      return generateLowerCase(this.text)
    },
    upperCaseText() {
      return generateUpperCase(this.text)
    },
  },
  methods: {
    handleDrawer() {
      this.showDrawer = !this.showDrawer
    },
  },
}
</script>

<style scoped>
.bg-blue-500 {
  background-color: #3b82f6;
}
</style>
