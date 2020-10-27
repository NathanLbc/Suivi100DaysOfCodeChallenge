<template>
  <div class="container">
    <div class="title">Async</div>

    <button
      class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
      v-on:click="asyncExample"
    >
      Async
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    asyncExample: function () {
      function external() {
        for (let i = 0; i < 30; i++) console.log(i)
      }

      async function test() {
        console.log('start')
        let resultat = await external()
        console.log('over')
      }
      test()
    },
  },
}
</script>
<style>
.container {
  text-decoration-color: blanchedalmond;
}
</style>
