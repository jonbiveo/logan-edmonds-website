<template>
  <div id="container">
    <div>
      <h1 id="name">Logan Edmonds</h1>
    </div>
    <div id="link-container">
      <a href="https://github.com/jonbiveo" target="_blank"><img class="links" src="../assets/github-brands.svg" alt="Github Link"></a>
      <a href="https://www.linkedin.com/in/logantedmonds/" target="_blank"><img class="links" src="../assets/linkedin-brands.svg" alt="LinkedIn Link"></a>
      <a href="mailto: logantedmonds@gmail.com"><img class="links" src="../assets/envelope-solid.svg" alt="E-Mail Link"></a>
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
  flex: 1;
  justify-content: space-around;
  align-items: center;
  background-color: blue;
}

#name {
  color: white;

}

.links {
  display: flexbox;
  width: 24px;
  justify-content: space-around;
  padding: 6px;
  color: white;
}

</style>