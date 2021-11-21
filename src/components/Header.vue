<template>
  <div id="header">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link :to="{ name: 'About' }">About</router-link> |
      <router-link :to="{ name: 'Contacts' }">Contacts</router-link>
    </div>
  </div>

</template>

<script>
export default {
  name: "Header"
}
</script>

<style>
#header {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 85px;
  background: white;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
  border-radius: 4px;
}

#nav a.router-link-exact-active {
  color: white;
  background: #2c3e50;
}
</style>