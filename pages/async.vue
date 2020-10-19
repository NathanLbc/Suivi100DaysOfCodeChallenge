<template>
  <div class="container">
    <button v-on:click="async">Async</button>
  </div>
</template>

<script>
export default {
  data: {
    tableauFake: [],
  },
  methods: {
    async: async function () {
      async function externe(){
        for (let i = 0; i<1000; i++)
        console.log(i)
      }


      async function programme(){
        console.log('start')
        let resultat = await externe();
        console.log('over')
        
      }
      programme();
    }
  }
}
</script>
