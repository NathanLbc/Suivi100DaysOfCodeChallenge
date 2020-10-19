<template>
  <div class="container">
    <button v-on:click="asyncExample">Async</button>
  </div>
</template>

<script>
export default {
  methods: {
    asyncExample: async function () {
      async function external(){
        for (let i = 0; i<1000; i++)
        console.log(i)
      }


      async function test(){
        console.log('start')
        let resultat = await external();
        console.log('over')
        
      }
      test();
    }
  }
}
</script>
