<template>
  <ul>
    <li v-for="pokemon in pokemonList">
      <RouterLink :to="`/about?name=${pokemon.name}`">{{ pokemon.name }}</RouterLink>
    </li>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      pokemonList: []
    }
  },
  async created() {
    const response = await fetch('https://pokeapi.co/api/v2/pokemon/')
    const result = await response.json()
    this.pokemonList = result.results
  }
}
</script>
