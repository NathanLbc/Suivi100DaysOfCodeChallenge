<template>
  <div class="container">
    <p id="officers">{{ result }}</p>
    <button v-on:click="totalYearsMethod">Total experience</button>
    <button v-on:click="mostExpericencedMethod">
      Who is the most experienced officer ?
    </button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      officers: [
        { id: 20, name: 'Captain Piett', years: 14 },
        { id: 24, name: 'General Veers', years: 30 },
        { id: 56, name: 'Admiral Ozzel', years: 16 },
        { id: 88, name: 'Commander Jerjerrod', years: 22 },
      ],
      result: [],
    }
  },
  methods: {
    totalYearsMethod: function () {
      console.log('click')
      this.result = this.officers.reduce(function (accumulator, officers) {
        return accumulator + officers.years
      }, 0)
    },
    mostExpericencedMethod: function () {
      console.log('Looking for the most experienced officer')
      this.result = this.officers.reduce(function (oldest, officers) {
        return (oldest.years || 0) > officers.years ? oldest : officers
      }, {})
    },
  },
}
</script>
