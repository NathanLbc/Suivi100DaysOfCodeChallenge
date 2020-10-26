<template>
  <div class="container">
   <title>Computed Properties</title>
   <div id="computed_props">
       
       FirstName : <input type="text" v-model = "firstname"/>
       LastName : <input type="text" v-model = "lastname" />
       <p> My name is {{ firstname }} {{ lastname }}</p>
       <p> Using computed method : {{ getfullname }}</p>


   </div>
  </div>

</template>

<script>
export default {
  el: "#computed_props",
  data() {
    return {
      firstname: "",
      lastname: "",
      birthyear: ""
  }
  },
  computed: {
      getfullname: function(){
          return this.firstname +" "+ this.lastname;
      }
  }
}
</script>
