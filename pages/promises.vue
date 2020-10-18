<template>
  <div class="container">
    <button v-on:click="creationData">Création des données</button>
    <button v-on:click="async">Fonction asynchrone</button>
    <li></li>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      tableauFake: [],
    }
  },
  methods: {
    creationData: function () {
      for (let i = 0; i < 1000; i++) {
        this.tableauFake.push({
          test: 'coucou : ' + i,
          number: 8,
        })
      }
    },
    async: function () {
      this.tableauFake.foreach(
        element => 
          console.log('ok'),
        
      setTimeout(this.element, 0),

      console.log("Hi there"),
      )
    },
  },
}
</script>
