<template>
  <div class="container">
    <div class="title">The different loops</div>
    <div class="subtitle">Classic loop for</div>
    <div>Open the console to check !</div>
    <button
      class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
      v-on:click="forLoop"
    >
      For Loop
    </button>
    <div class="subtitle">For In Loop (with NuxtJS)</div>
    <li
      id="officers"
      class="white-text"
      v-for="officer in officers"
      :key="officer.name"
    >
      {{ officer.name }}
    </li>
    <div class="subtitle">While Loop</div>
    <button
      class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
      v-on:click="whileLoop"
    >
      While Loop
    </button>
    <div class="subtitle">Do While Loop</div>
    <button
      class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
      v-on:click="doWhileLoop"
    >
      Do While Loop
    </button>
    <div class="subtitle">For Of Loop</div>
    <button
      class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
      v-on:click="forOfLoop"
    >
      For Of Loop
    </button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      officers: [
        { id: 20, name: 'Captain Piett', years: 14, status: 'alive' },
        { id: 24, name: 'General Veers', years: 30, status: 'dead' },
        { id: 56, name: 'Admiral Ozzel', years: 16, status: 'alive' },
        { id: 88, name: 'Commander Jerjerrod', years: 22, status: 'alive' },
      ],
    }
  },
  methods: {
    forLoop: function () {
      console.log("for loop start")
      for (let i = 0; i <= 5; i++) {
        
        console.log(i)
      }
    },
    whileLoop: function() {
        let i = 0;
        console.log("while loop start")
        while(i <= 5) {
            i++;
            console.log(i)
        }
        console.log("success")
    },
    doWhileLoop: function (){
        console.log("Do While Loop start")
        let result = '';
        let i = 0;
        do {
            i = i + 1;
            result = result + i;
        } while (i<5);
        console.log(result)
    },
    forOfLoop: function() {
        console.log("For Of Loop");
        for (let element of officers) {
            console.log(element);
        }
    }
  },
}
</script>

<style></style>
