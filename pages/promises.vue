<template>
  <div class="container">
    <div class="title">Promises</div>

    <button
      class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
      v-on:click="promiseTest"
    >
      Promise
    </button>
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
          resolve('foo')
        }, 1000)
      })
      promise1.then((value) => {
        this.promise.push(value)
      })
    },
  },
}
</script>
