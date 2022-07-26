<template>
  <div class="app">
    <h2>Composition API</h2>
    <p>Name: {{ name }}</p>
    <p>Number of dogs: {{ numberOfDogs }}</p>
    <p>Age: {{ age }}</p>
    <p>Is admin? {{ isAdmin }}</p>
    <p>Little text: {{ randomInfo }}</p>
    <button @click="changeValues('Italo', 22, 7, true)">Change Values</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref } from 'vue'

export default defineComponent({
  name: 'TsWithCompositionAPI',
  setup() {
    const state = reactive({
      name: 'Teste' as string,
      age: 25 as string | number,
      numberOfDogs: '4' as string | number,
      isAdmin: false as boolean
    })

    const randomInfo = ref<string | number>('lorel ipsum bla bla bla')

    function changeValues(
      name: string,
      age: number,
      numberOfDogs: number,
      isAdmin: boolean
    ) {
      state.name = name
      state.age = age
      state.numberOfDogs = numberOfDogs
      state.isAdmin = isAdmin
    }

    return {
      //functions
      changeValues,

      //variables
      randomInfo,
      ...toRefs(state)
    }
  }
})
</script>
<style scoped>
.app {
  background: #22cc88;
  color: #e9f8ed;
  width: 100%;
}
</style>
