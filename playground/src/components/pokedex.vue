<!-- eslint-disable vue/multi-word-component-names -->
<script>
// https://pokeapi.co/api/v2/pokemon?limit=151

export default {
  async setup() {
    const regionName = 'kanto'
    const pokedex = await fetch('https://pokeapi.co/api/v2/pokemon?limit=151').then(response =>
      response.json()
    )

    return {
      pokedex,
      regionName
    }
  },
  created() {
    console.log(this.regionName)
    console.log(this.pokedex)
  }
}
</script>
<template>
  <h2>{{ regionName }}</h2>
  <pre>{{ pokedex }}</pre>
</template>
