<template>
  <div class="post" v-for="postItem in postList" :key="postItem.id">
    <div class="post-info">
      <img class="post-author-photo" :src="(postItem.authorPhoto != null) ? postItem.authorPhoto : require('@/assets/user.png')">
      <p class="date">{{ postItem.date }}</p>
    </div>
    <img class="post-image" v-bind:src="postItem.image">
    <p class="post-text">{{ postItem.text }}</p>
    <button class="like-button" v-on:click="LikeClick(postItem.id)">{{ postItem.likes }}</button>
  </div>
</template>

<script>
export default {
  data:function () {
    return {}
  },
  computed: {
    postList(){
      return this.$store.state.postList
    }
  },

  methods: {
    /*
    LikeClick: function (id) {
      this.$store.state.postList.forEach(post => {
        if (post.id === id) post.likes += 1;
      });
    }*/
    LikeClick: function (id) {
      this.$store.dispatch("IncreaseLikesAct", id);
    }
  }
}
</script>

<style>
.post {
  min-width: 450px;
  width: 60%;
  max-width: 720px;
  background-color: #ffffff;
  margin: 30px auto auto;
  box-shadow: 0 0 10px 1px #888888;

  padding: 20px;

  text-align: start;
}

.post-info {
  display: flex;
  flex-direction: row;
}

.post-author-photo {
  width: 50px;
  height: 50px;
  vertical-align: middle;
  margin-bottom: 10px;
  text-align: start;
  border-radius: 100%;
}

.date {
  margin-left: auto;
  font-size: 15px;
  font-style: italic;
}

.post-image {
  width: 100%;
}

.post-text {
  font-size: 22px;
}


.like-button {
  background-image: url(../assets/like.png);
  background-size: 24px;
  background-repeat: no-repeat;
  background-position: 20% 50%;
  background-color: steelblue;
  width: 75px;
  height: 30px;
  text-align: end;
  font-size: 14px;
  color: white;
  font-weight: bold;

  border: none;
  border-radius: 3px;
}

.like-button:hover {
  background-color: royalblue;
}
</style>