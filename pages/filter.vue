<template>
  <div class="container">
    <li v-for="officer in officers" :key="officer.Index">{{ officers }}</li>
    <li id="officers" v-for="officer in officersStatus" :key="officer.name">{{ officer.name }}</li>
    <button v-on:click="deadOfficerMethod">Who is dead ?</button>
    <button v-on:click="aliveOfficerMethod">Who is still alive ?</button>

  </div>
</template>

<script>
export default {
  data: function () {
    return {
      officers: [
        { id: 20, name: 'Captain Piett', years: 14, status: "alive"},
        { id: 24, name: 'General Veers', years: 30, status: "dead" },
        { id: 56, name: 'Admiral Ozzel', years: 16, status: "alive" },
        { id: 88, name: 'Commander Jerjerrod', years: 22, status: "alive" },
      ],
      officersStatus: [],
    }
  },
  methods: {
    deadOfficerMethod: function () {
        console.log("dead");
      this.officersStatus = this.officers.filter(function (officers) {
        return officers.status === "dead";
      })
    },
    aliveOfficerMethod: function () {
        console.log("alive");
      this.officersStatus = this.officers.filter(function (officers) {
        return officers.status === "alive";
      })
    }
  },
}
</script>
