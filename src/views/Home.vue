<template>
  <div class="home">
    <img class="logo" alt="Vue logo" src="../assets/Rephil_03_final_RGB.svg" >
    <Hello />
  </div>
</template>

<script>
// @ is an alias to /src
import Hello from "../components/HelloWorld"

export default {
  name: 'home',
  components: {
    Hello
  }
}
</script>

<style lang="scss" scoped>

.home {
  display: flex;
  justify-content: center;
  
  .logo {
    padding-top: 1rem;
    width: 200px;
  }
}

</style>

