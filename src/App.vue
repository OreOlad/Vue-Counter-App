<template>
  <div>
    <Header />
    <section class="main-section">
      <Count v-bind:count="this.count" v-bind:adds="this.adds" v-bind:minuses="this.minuses" v-on:raise-count="raiseCount()" v-on:lower-count="lowerCount()"/>
    </section>
  </div>
</template>


<script>
  import Header from "./components/header.vue";
  import Count from "./components/count.vue";
  export default {
    name: "App",
    components: {
      Header,
      Count
    },
    data() {
      return{
        count: 0,
        adds: 0,
        minuses: 0
      };
    },
    methods: {
      lowerCount() {
        this.count = this.count - 1;
        this.minuses = this.minuses + 1;
      },
      raiseCount() {
        this.count = this.count + 1;
        this.adds = this.adds + 1;
      }
    }
  }
</script>

<style>
  * {
    box-sizing: border-box;
  }
  html, body {
    margin: 0;
  }
  .main-section {
    display: flex;
    justify-content: center;
    margin-top: 3rem;
  }
</style>

