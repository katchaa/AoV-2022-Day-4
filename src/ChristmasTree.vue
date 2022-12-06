<template>
  <div>
    <div v-for="line in size" :key="line" class="flex justify-center">
      <div
        v-for="point in line"
        :key="point"
        class="rounded-full bg-green w-16 h-16 -m-2 flex justify-center items-center"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
withDefaults(
  defineProps<{
    size: number | undefined
  }>(),
  {
    size: 1,
  }
)
</script>
