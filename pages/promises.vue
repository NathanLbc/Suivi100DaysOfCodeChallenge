<template>
  <div class="container">
    <button v-on:click="promiseTest">Promise</button>
    <li>{{ promise }}</li>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      
        promise: [],
      
    }
  },
  methods: {
    promiseTest: function () {
      
      const promise1 = new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve('foo');
        }, 1000);
      });
      promise1.then((value) => {
        this.promise.push(value)
      });
      
    },
    
  },
}
</script>
