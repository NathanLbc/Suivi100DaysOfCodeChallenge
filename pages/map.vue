<template>
  <div class="container">
    <p id="officers">{{ officersId }}</p>
    <button v-on:click="officersIdMethod">Activate</button>
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
        console.log("click");
      this.officersId = this.officers.map(function (officers) {
        return officers.id
      })
    },
  },
}
</script>
