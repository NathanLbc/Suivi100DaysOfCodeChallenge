<template>
  <div class="container">
    <p id="officers">{{ result }}</p>
    <button class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded" v-on:click="totalYearsMethod">Total experience</button>
    <button class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded" v-on:click="mostExpericencedMethod">
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
