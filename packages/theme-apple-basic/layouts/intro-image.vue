<script setup lang="ts">
import { computed, defineProps } from 'vue'
import { handleBackground } from '../layoutHelper'
const props = defineProps({
  image: {
    type: String,
  },
})
const style = computed(() => handleBackground(props.image))
</script>

<template>
  <div class="slidev-layout w-full h-full intro-image" :style="style">
    <slot />
  </div>
</template>
