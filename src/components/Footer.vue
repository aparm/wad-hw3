<template>
  <div id="footer">
    <router-link :to="{ name: 'Contacts' }">Contact us</router-link>
  </div>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style>
#footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 40px;
  background-color: aquamarine;

  padding-top: 20px;
}

#footer a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
  border-radius: 4px;
}

#footer a:hover {
  color: white;
  background: #2c3e50;
}

</style>