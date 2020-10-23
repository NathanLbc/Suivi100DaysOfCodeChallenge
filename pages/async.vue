<template>
  <div class="container">
    <button v-on:click="asyncExample">Async</button>
  </div>
</template>

<script>
export default {
  methods: {
    asyncExample: function () {
      function external(){
        for (let i = 0; i<30; i++)
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
