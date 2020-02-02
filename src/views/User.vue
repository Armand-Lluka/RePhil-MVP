<template>
  <div>
    <MaleAvatar class="user-image" />
    <h1>Hello {{id}}</h1>
  </div>
</template>

<script>
import MaleAvatar from "../components/svg-components/MaleAvatar"
export default {
  name: "User",
  components: {
      MaleAvatar
  },
  created(){
      console.log(this.$route)
  },
  props: ['id']
};
</script>

<style lang="scss" scoped>
 .user-image {
     width: 300px;
 }
</style>
