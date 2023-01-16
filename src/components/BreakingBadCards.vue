<script setup>
  import axios from "axios"
//A note about not needing async syntax for awaiting the response. 
//The composition API & script setup, they are automatically async + await. 
  const response = await axios.get("https://www.breakingbadapi.com/api/character/random")

  console.log(response)
</script>

<template>
  <div>
    <h1>Breaking Bad Cards</h1>
  </div>
</template>