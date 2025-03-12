<template>
  <section class="min-h-screen flex flex-col justify-center items-center bg-blue-950 text-white">
    <div class="h-96 w-96 grid grid-cols-2">
      <div class="bg-amber-100 hidden md:block xl:block">
        <img src="/images/bg-login.jpg" alt="Authentication" class="w-auto h-full object-cover" />
      </div>
      <div
        class="bg-cyan-800 p-4 w-96 border-1 border-t-slate-400 border-b-slate-400 border-r-slate-400 border-l-slate-400 md:border-l-0 rounded-2xl md:rounded-none"
      >
        <div class="mb-2 text-center text-2xl">Sign Up</div>
        <p class="text-slate-400">Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
        <div class="mt-3">
          <form>
            <div class="mb-3">
              <label for="name" class="block">Name</label>
              <input
                type="text"
                id="name"
                class="w-full p-1 border-1 border-b-slate-400 border-t-0 border-l-0 border-r-0"
              />
            </div>
            <div class="mb-3">
              <label for="email" class="block">Email</label>
              <input
                type="email"
                id="email"
                class="w-full p-1 border-1 border-b-slate-400 border-t-0 border-l-0 border-r-0"
              />
            </div>
            <div class="mb-3">
              <label for="password" class="block">Password</label>
              <input
                type="password"
                id="password"
                class="w-full p-1 border-1 border-b-slate-400 border-t-0 border-l-0 border-r-0"
              />
            </div>
            <div class="mb-3">
              <label for="confirm_password" class="block">Confirm Password</label>
              <input
                type="password"
                id="confirm_password"
                class="w-full p-1 border-1 border-b-slate-400 border-t-0 border-l-0 border-r-0"
              />
            </div>
            <div class="mb-3">
              <button
                type="submit"
                class="w-full bg-amber-500 px-2 py-3 rounded-2xl cursor-pointer"
              >
                Sign Up
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    return {}
  },
}
</script>
