<template>
  <div>
    <CompositionAPI />
    <OptionsAPI />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CompositionAPI from './components/TsWithCompositionAPI.vue'
import OptionsAPI from './components/TsWithOptionsAPI.vue'

export default defineComponent({
  components: {
    CompositionAPI,
    OptionsAPI
  }
})
</script>