<script setup>
const props = defineProps({
  title: String,
  description: String,
  items: Array,
});
</script>

<template>
  <h2
    class="text-4xl font-bold text-center text-zinc-800 sm:text-6xl"
    v-if="title"
  >
    {{ title }}
  </h2>
  <p
    class="max-w-3xl mx-auto my-10 text-xl text-center text-zinc-500"
    v-if="description"
  >
    {{ description }}
  </p>
  <div class="grid gap-6 mt-10 mb-20 md:grid-cols-3">
    <div
      v-for="item of items"
      class="p-4 border-2 border rounded-lg shadow-md border-zinc-300 sm:p-8 bg-blue-100/30"
    >
      <div class="flex items-center justify-between mb-4 gap-x-3">
        <Icon class="w-8 h-8" v-if="item.icon" :name="item.icon" />
        <span class="text-md text-white bg-blue-500/70 rounded-md px-2 py-1" v-if="item.label">{{ item.label }}</span>
      </div>
      <h3 class="text-2xl font-semibold text-zinc-800" v-if="item.title">
        {{ item.title }}
      </h3>
      <p class="mt-2 leading-relaxed text-zinc-500" v-if="item.description">
        {{ item.description }}
      </p>
    </div>
  </div>
</template>
