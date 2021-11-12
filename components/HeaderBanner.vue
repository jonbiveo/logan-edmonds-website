<template>
  <div id="container">
    <div>
      <h1 id="name">Logan Edmonds</h1>
    </div>
    <div id="link-container">
      <a href="https://github.com/jonbiveo" target="_blank"><font-awesome-icon class="links" :icon="['fab', 'github-square']"></font-awesome-icon></a>
      <a href="https://www.linkedin.com/in/logantedmonds/" target="_blank"><font-awesome-icon class="links" :icon="['fab', 'linkedin']"></font-awesome-icon></a>
      <a href="mailto: logantedmonds@gmail.com"><font-awesome-icon class="links" :icon="['fas', 'envelope']"></font-awesome-icon></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderBanner',
}
</script>

<style scoped>

#container {
  display: flex;
  position: absolute;
  justify-content: space-around;
  align-items: center;
  background-color: rgb(16, 20, 25, 0.8);
  max-width: 100% !important;
  width: 100% !important;
  left: 0;
  right: 0;
  top: 0;
  border-bottom: black;
  border-bottom: 4px solid black;
}

#name {
  color: white;
  margin: 30px 50px;
}

.links {
  display: flexbox;
  /* width: 20px; */
  font-size: 20px;
  justify-content: space-around;
  padding: 6px;
  color: white;
}

</style>