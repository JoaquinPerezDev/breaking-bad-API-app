<script setup>
  import axios from "axios"
  import { ref, watch } from "vue"

  const characters = ref(null)
  const page = ref(0)
//A note about not needing async syntax for awaiting the response. 
//The composition API & script setup, they are automatically async + await. 
  const response = await axios.get("https://www.breakingbadapi.com/api/characters?limit=8")
  characters.value = response.data

  watch(page, async () => {
    const res = await axios.get(`https://www.breakingbadapi.com/api/characters?limit=8&offset=${page.value * 8}`)
  })

</script>

<template>
  <div>
    <h1>Breaking Bad Cards</h1>
    <h1>{{characters}}</h1>
    <div>
      <button @click="page = page + 1">Next</button>
      <button @click="page = page - 1">Back</button>
    </div>
  </div>
</template>