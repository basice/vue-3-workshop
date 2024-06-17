<script>
export default {
  data() {
    return {
      count: 10,
      counterTitle: 'Counter Standard',
      incrementAmount: 8,
      message: 'Hello it works',
      listOfNumbers: [
        {
          name: 1,
          id: '6a887cd2-f0bf-4321-b192-92016f82a883',
          list: [1, 2, 3]
        },
        {
          name: 2,
          id: '8d14d90b-2d47-473e-8293-d5c324111d0d',
          list: [1, 2, 3]
        },
        {
          name: 3,
          id: 'cd806d65-2309-4625-9104-dcd636cd79b5',
          list: [1, 2, 3]
        },
        {
          name: 4,
          id: '00c939cd-fbf4-46d0-8e61-0bc2ce8a5332',
          list: [1, 2, 3]
        },
        {
          name: 5,
          id: '295a8170-59c1-4462-9de1-3c9cd41cedab',
          list: [1, 2, 3]
        }
      ]
    }
  }
}
</script>

<template>
  <h1>{{ displayTitle }}</h1>
  <p :data-increment-by="incrementAmount">{{ count }}</p>
  <button @click="incrementCount">Increment Count</button>
  <h1>{{ incrementAmount }}</h1>
  <p>{{ optimizedIncrementAmount }}</p>
  <div>
    <label for="incrementAmount">Increment by:</label>
    <input
      type="text"
      v-model="incrementAmount"
    />
  </div>
  <hr />
  <p v-if="message.length % 2 === 0">Even: {{ message.toUpperCase() }}</p>
  <p v-else>Odd: {{ message }}</p>
  <ul
    v-for="(item, index) in listOfNumbers"
    v-bind:key="`item-${index}`"
  >
    <li>
      {{ item.id }}
      <ul>
        <li
          v-for="(number, index) in item.list"
          v-bind:key="`number-${index}`"
        >
          {{ number }}
        </li>
      </ul>
    </li>
  </ul>
</template>

<style scoped></style>
