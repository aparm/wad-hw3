<template>
  <div class="home">
    <h1>Home page</h1>
    <Posts></Posts>
    <button class="reset-likes" v-on:click="ResetLikes">Reset Likes!</button>
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
  },

  methods: {
    ResetLikes: function () {
      this.$store.dispatch("ResetLikesAct");
    }
  }
}
</script>

<style>
.home {
  margin-bottom: 80px;
}

.reset-likes {
  font-weight: bold;
  background: steelblue;
  color: white;
  border: none;
  padding: 10px;
  margin: 20px;
  border-radius: 4px;
}

.reset-likes:hover {
  background: #2c3e50;
}

</style>
