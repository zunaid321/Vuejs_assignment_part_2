<template>
  <div>
    <b-table striped hover :items="items"></b-table>
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
