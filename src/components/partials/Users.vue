<template>
  <section class="h-auto flex flex-col items-center justify-center bg-slate-900">
    <div>
      <h1 class="text-3xl font-bold text-white text-center m-8">Users</h1>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
        <div
          v-for="user in users.slice(0, 6)"
          :key="user.id"
          class="bg-slate-800 text-white rounded-lg shadow-md p-6 border-1 border-cyan-300 hover:bg-slate-700 hover:border-cyan-500 cursor-pointer"
        >
          <h2 class="text-xl font-bold">{{ user.name }}</h2>
          <p class="text-sm">{{ user.email }}</p>
          <p class="text-sm">{{ user.phone }}</p>
          <p class="text-sm">{{ user.website }}</p>
          <p class="text-sm">{{ user.company.name }}</p>
          <p class="text-sm">
            {{ user.address.street }}, {{ user.address.suite }}, {{ user.address.city }},
            {{ user.address.zipcode }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Users',
  data() {
    return {
      users: [],
    }
  },
  async created() {
    try {
      const response = await fetch('https://jsonplaceholder.typicode.com/users')
      this.users = await response.json()
    } catch (error) {
      console.error('Error fetching users:', error)
    }
  },
}
</script>

<style scoped>
/* Add any custom styles here */
</style>
