<script>
export default {
  data: () => ({
    newCharacter: { name: '', element: [] },
    characterList: [
      {
        name: 'Aang',
        element: ['Air', 'Earth', 'Water', 'Fire']
      },
      {
        name: 'Zuko',
        element: ['Fire']
      },
      {
        name: 'Toph',
        element: ['Earth']
      },
      {
        name: 'Katara',
        element: ['Water']
      }
    ],
    favoriteList: []
  }),
  computed: {
    benderStatistics() {
      const elements = ['Air', 'Earth', 'Fire', 'Water']

      const statistics = {
        Air: 0,
        Earth: 0,
        Water: 0,
        Fire: 0
      }

      this.characterList.forEach((character) => {
        elements.forEach((element) => {
          if (character.element.indexOf(element) > -1) {
            statistics[element] += 1
          }
        })
      })

      return statistics
    }
  },
  methods: {
    addNewCharacter() {
      this.characterList.push(this.newCharacter)
      this.newCharacter = { name: '' }
    },
    favoriteCharacter(character) {
      this.favoriteList.push(character)
    }
  }
}
</script>

<template>
  <h2>Statistics</h2>
  <ul>
    <li
      v-for="(stat, type, index) in benderStatistics"
      v-bind:key="`stat-${index}`"
    >
      {{ type }} : {{ stat }}
    </li>
  </ul>

  <h2>Characters</h2>

  <p v-if="characterList.length === 0">There are no characters</p>
  <ul v-else-if="characterList.length % 2 === 0">
    <li
      v-for="(character, index) in characterList"
      v-bind:key="`character-${index}`"
    >
      <p>{{ character.name }}</p>
      <button @click="favoriteCharacter(character)">⭐ Favorite</button>
    </li>
  </ul>
  <p v-else>There are odd characters!</p>

  <p>
    <span
      v-for="(character, index) in characterList"
      v-bind:key="`character-${index}`"
      >{{ character.name }}{{ index === characterList.length - 1 ? '' : ', ' }}
    </span>
  </p>

  <h2>Favorite Caharcters</h2>
  <ul v-if="favoriteList.length > 0">
    <li
      v-for="(character, index) in favoriteList"
      v-bind:key="`character-${index}`"
    >
      {{ character }}
    </li>
  </ul>
  <p v-else>No favorite characters yet!</p>

  <h2>New character</h2>
  <pre>{{ newCharacter }}</pre>
  <label for="character-name">Name</label>
  <input
    type="text"
    v-model="newCharacter.name"
    @keyup.enter="addNewCharacter()"
  />
</template>

<style scoped></style>
