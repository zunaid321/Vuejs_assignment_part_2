<template>
  <div>
    <b-table striped hover :items="items"></b-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          ID: 1,
          Student_Names: "Zunaid",
          Math: 74,
          Physics: 70,
          Chemistry: 79,
          English: 80,
          Marks: 70,
          Final_Score: 79,
          Grade: "C"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
