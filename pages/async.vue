<template>
  <div class="container">
      <button v-on:click="async">Async</button>
  </div>
  
</template>

<script>
export default {
  methods: {
    async: function () {
    const logName = () => {
      console.log("Han")
      }
    setTimeout(logName, 0);
    console.log("Hi there");
    }
    }
  }

</script>
