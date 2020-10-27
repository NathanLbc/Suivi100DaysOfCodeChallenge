<template>
  <div class="container">
    <div class="title">asyncData</div>
    <button
      class="bg-transparent hover:bg-grey-500 text-grey-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
      v-on:click="asyncData"
    >
      Get top tweets
    </button>
    <div>{{ Trend }}</div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data: function () {
    return {
      Trend: [],
    }
  },
  methods: {
    asyncData: async function () {
      const config = {
        headers: {
          Authorization: `Bearer AAAAAAAAAAAAAAAAAAAAAKOhJAEAAAAA3y%2BbfsTJswACJBBQv5uoXCeHsmQ%3DwyEvUoV6q93REinnLI8VCD515ltjuZkuOzIOotwArCNptJ2S9y`,
        },
      }
      let topTweet = ''
      let globalData = ''
      let item = ''

      await axios
        .get('/api/1.1/trends/place.json?id=1', config)
        .then((response) => {
          globalData = response.data[0].trends
          for (item of globalData) {
            topTweet += '\n' + item.name + ', '
          }
          console.log(topTweet)
        })
      this.Trend.push(topTweet)
    },
  },
}
</script>

<style>
.title {
  margin-bottom: 30px;
}
</style>
