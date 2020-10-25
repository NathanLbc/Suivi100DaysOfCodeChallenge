<template>
  <div class="container">
    <ul>
      <li v-for="officer in officers" :key="officer.Index">
        <div>{{ officer }}</div>
      </li>
    </ul>
    <p id="officers">{{ officersId }}</p>
    <button class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded" v-on:click="officersIdMethod">Activate</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      officers: [
        { id: 20, name: 'Captain Piett' },
        { id: 24, name: 'General Veers' },
        { id: 56, name: 'Admiral Ozzel' },
        { id: 88, name: 'Commander Jerjerrod' },
      ],
      officersId: [],
    }
  },
  methods: {
    officersIdMethod: function () {
      console.log('click')
      this.officersId = this.officers.map(function (officers) {
        return officers.id
      })
    },
  },
}
</script>
