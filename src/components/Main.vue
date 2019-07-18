<template>
  <main class="main">
    <Profile />
    <Ad />
  </main>
</template>

<script>
import Profile from './Profile'
import Ad from './Ad'

export default {
  name: 'Main',
  components: {
    Profile,
    Ad
  }
}
</script>

<style scoped>
.main {
  margin: 16px auto 0;
  max-width: 1136px;
  display: flex;
  justify-content: space-between;
}
</style>
