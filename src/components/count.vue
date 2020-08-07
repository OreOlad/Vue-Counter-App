<template>
  <div>
    <h4>My Count is {{count}}</h4><br/>
    <h4>My Adds are {{adds}}</h4><br/>
    <h4>My Minuses are {{minuses}}</h4><br/>
    <section> <button @click="$emit('raise-count')">Raise Count</button> <button @click="$emit('lower-count')">Lower Count</button></section>
  </div>
</template>

<script>
export default {
  name: "Count",
  props: ["count", "adds", "minuses"]
};
</script>

<style scoped>
  div {
    width: 30rem;
    height: 30rem;
    border: 1px solid lightgrey;
    border-radius: 1.25rem;
    padding: 5rem;
    text-align:center;
    font-family: "Nova Mono";
  }
  h4 {
    width: fit-content;
  }

</style>

