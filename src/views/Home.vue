<template>
  <div class="home">
    <h1>Home page</h1>
    <Posts></Posts>
  </div>
</template>

<script>

import Posts from "../components/Posts";
export default {
  name: 'Home',
  components: {Posts},
  props: ["postList"],
  data(){
    return{}
  }
}
</script>

<style>
.home {
  margin-bottom: 80px;
}
</style>
