<template>
  <div class="app">
    <h2>Options API</h2>
    <p>Name: {{ name }}</p>
    <p>Number of dogs: {{ numberOfDogs }}</p>
    <p>Age: {{ age }}</p>
    <p>Is admin? {{ isAdmin }}</p>
    <button @click="changeValues('Italo', 22, 7, true)">Change Values</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'TsWithOptionsAPI',
  data() {
    return {
      name: 'Italo' as string,
      numberOfDogs: '2' as string | number,
      age: '22' as string | number,
      isAdmin: false as boolean
    }
  },
  methods: {
    changeValues(
      name: string,
      numberOfDogs: number,
      age: number,
      isAdmin: boolean
    ) {
      this.name = name
      this.numberOfDogs = numberOfDogs
      this.age = age
      this.isAdmin = isAdmin
    }
  }
})
</script>
<style scoped>
  .app{
    background: #2288bb;
    color: white;
    width: 100%;
  }
</style>