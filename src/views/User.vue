<template>
  <div>
    <MaleAvatar class="user-image" />
    <h1>Hello {{user.username}}</h1>
    <qrcode value="Hello, World!" :options="{ 'max-width': '100%', width: 300 }"></qrcode>
  </div>
</template>

<script>
import MaleAvatar from "../components/svg-components/MaleAvatar"
import axios from 'axios';

export default {
  name: "User",
  data: function(){
      return {
          user: Object
      }
  },
  components: {
      MaleAvatar
  },
  async mounted(){
    // console.log(this.$route)
    let param = this.$route.params.id

    const {data} = await axios.get(`http://127.0.0.1:63011/users/${param}`)
    this.user = data

    console.log(param)
    console.log(this.user)
  },
  props: {
      id: String
  }
};
</script>

<style lang="scss" scoped>
 .user-image {
     width: 300px;
 }
</style>
