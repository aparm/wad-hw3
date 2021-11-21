<template>
  <div class="home">
    <h1>Home page</h1>
    <Post authorPhoto="https://raw.githubusercontent.com/Ashwinvalento/cartoon-avatar/master/lib/images/male/45.png" date="14.02.2021 05:37" id="33" likes="1000" image="https://pics.me.me/when-you-actually-the-read-the-documentation-sometimes-my-genius-is-its-48199681.png" text="Test"></Post>
  </div>
</template>

<script>

import Post from "../components/Post";
export default {
  name: 'Home',
  components: {Post}
}
</script>
