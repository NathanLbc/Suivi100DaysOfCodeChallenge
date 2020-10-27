<template>
  <div class="container">
    <div class="title">Computed</div>

    <div>
      FirstName : <input type="text" v-model="firstname" /> LastName :
      <input type="text" v-model="lastname" />
      <p>My name is {{ firstname }} {{ lastname }}</p>
      <p>Using computed method : {{ getfullname }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstname: '',
      lastname: '',
      birthyear: '',
    }
  },
  computed: {
    getfullname: function () {
      return this.firstname + ' ' + this.lastname
    },
  },
}
</script>
