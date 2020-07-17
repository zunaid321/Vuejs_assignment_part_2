<template>

<div class="px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
    <h1 class="display-4">Results</h1>
    <p class="lead">Congrats on your results! If you don't like your results down below, feel free to take the quiz again!</p>


    <h1 class="Quiz">HSC Exam</h1>
    <h2 class="Name">Anonymous</h2>



  <div>
    <b-table :items="items"></b-table>
  </div>  


</div>


</template>

<script>
import marks from "./json/data.json";

export default {
  name: "student marks",
  data() {
    return {
      items: marks
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
