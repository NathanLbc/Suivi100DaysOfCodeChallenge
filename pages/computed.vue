<template>
  <div class="container">
   <title>Computed Properties</title>
   <div id="computed_props">
       
       
       <button v-on:click="getfullname">Update</button>
       FirstName : <input type="text" v-model = "fistname"/>
       LastName : <input type="text" v-model = "lastname" />
       <p> My name is {{ firstname }} {{ lastname }}</p>
       <p> Using computed method : {{getfullname}}</p>


   </div>
  </div>

</template>

<script>
export default {
  el: "#computed_props",
  data: {
      firstname: "",
      lastname: "",
      birthyear: ""
  },
  computed: {
      getfullname: function(){
          return this.firstname +" "+ this.lastname;
      }
  }
}
</script>
