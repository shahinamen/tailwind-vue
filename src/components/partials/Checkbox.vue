<template>
  <section class="h-screen flex flex-col justify-center items-center bg-slate-100">
    <div>
      <div class="flex items-center">
        <input type="checkbox" class="custom-checkbox" id="checkbox" v-model="checked" />
        <label for="checkbox" class="ml-2 block text-sm text-gray-900">Checkbox</label>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      checked: false,
    }
  },
}
</script>
<style scoped>
/* Custom checkbox styling */
.custom-checkbox {
  appearance: none; /* Remove default styling */
  -webkit-appearance: none;
  -moz-appearance: none;
  width: 20px;
  height: 20px;
  border: 2px solid red; /* Red border */
  border-radius: 4px;
  cursor: pointer;
  position: relative;
}

/* Blue fill when checked */
.custom-checkbox:checked {
  background-color: cyan; /* Blue fill */
  border-color: cyan; /* Optional: Change border color when checked */
}

/* Checkmark styling (optional) */
.custom-checkbox:checked::after {
  content: '✔';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white; /* White checkmark */
  font-size: 14px;
}
</style>
