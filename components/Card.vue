<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  type: {
    type: String,
  }
})

const counter = ref(props.count)
</script>

<template>
  <div flex="~ col" border="~ main rounded-md" p="4">
    <h1>
        <carbon:idea v-if="type === 'idea'"/>
        <carbon:warning-alt v-if="type === 'warning'"/>
        <slot/>
    </h1>
    <slot name="content"/>
  </div>
</template>
