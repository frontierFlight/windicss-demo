<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
  <div class="p-5px pt-[0.3px]">这是文本啊这是文本啊这是文本啊</div>

  <button class="bg-hex-b2a8bb">按钮颜色</button>
  <button class="bg-[hsl(211.7,81.9%,69.6%)]">按钮颜色</button>

  <div class="grid-cols-[auto,1fr,30px]">grid</div>

  <div class="bg-white dark:hover:(bg-gray-800 font-medium text-white)">Variant Groups</div>
  <div class="bg-white dark:hover:bg-gray-800 dark:hover:font-medium dark:hover:text-white">Variant Groups</div>

  <div class="p-1 md:p-2 <lg:p-3">Responsive Design</div>

  <div class="!text-red-400 text-green-400">Green important</div>

  <div class="btn hover:btn-green">Shortcuts</div>

  <div class="text-black dark:text-white">Dark Mode</div>

  <div class="text-green-400 rtl:(text-red-400 text-right)">RTL RTL RTL RTL</div>

  <button class="test-btn">@apply usage</button>

  <button
    w:bg="blue-400 hover:blue-500 dark:blue-500 dark:hover:blue-600"
    w:text="sm white"
    w:font="mono light"
    w:p="y-2 x-4"
    w:border="2 rounded blue-200"
  >
    Button width attributify
  </button>
</template>

<style scoped>
.test-btn {
  @apply font-bold py-2 px-4 rounded;
}
.btn-blue {
  @apply bg-blue-500 hover:bg-blue-700 text-white;
  padding-top: 1rem;
}
</style>
