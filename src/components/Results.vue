<template>

<div class="px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
    <h1 class="display-4">Results</h1>
    <p class="lead">Congrats on your results! If you don't like your results down below, feel free to take the quiz again!</p>


    <h1 class="Quiz">HSC Exam</h1>
    <h2 class="Name">Anonymous</h2>

  <div class="table">
    <b-table :items="items"></b-table> 
  </div>


  <div class="result">
    <p>
      Correct:
      <strong>{{ totalCorrect }}</strong>
    </p>
  </div>

  <div class="result">
    <p>
      Marks Deducted:
      <strong>{{ totalWrong }}</strong>
    </p>
  </div>    

  <div class="result">
    <p>
      Total:
      <strong>{{ totalMarks }}/40</strong>
    </p>
  </div>    

</div>


</template>

<script>
import marks from "./json/data.json";

export default {
  name: "student_marks",
  data()
  {
    return {
      items: marks
      
    };
  },

computed: {
   totalMarks(){
     var correct = 0
     var wrong = 0
     var total = 0
     if(this.items){
       this.items.forEach(element => {
       correct += parseInt(element.Correct)
       wrong += parseInt(element.Wrong)
     })
     total = correct - (0.25*wrong)
     }
     return total
   },

   totalCorrect(){
     var tc = 0
     if(this.items){
       this.items.forEach(element => {
       tc += parseInt(element.Correct)
     })
     }
     return tc
   },

   totalWrong(){
     var tw = 0
     if(this.items){
       this.items.forEach(element => {
       tw += parseInt(element.Wrong)
     })
     }
     return (tw*0.25)
   }

   
}




};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .result{
    margin-left: 35%;
    font-size: 2rem;
  }
  .table{
    width: 70%;
    margin-left: 15%;
  }  
</style>
