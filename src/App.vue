<template>
  <div id="app">
    <Header/>
    <Main />
  </div>
</template>

<script>
import Header from './components/Header'
import Main from './components/Main'

export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Abel', sans-serif;
}

a {
  font-size: 14px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.29;
  letter-spacing: 0.5px;
  color: #282a36;
  text-decoration: none;
}

body {
  max-width: 1440px;
  margin: 0 auto;
  background: #f3f4f6;
}
</style>
