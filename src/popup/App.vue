<template>
  <div id="app">
    Loading...
  </div>
</template>

<script>
export default {
  created () {
    chrome.cookies.set({
      name: 'ASP.NET_SessionId',
      url: 'https://t.2c2p.com/RedirectV3/Payment/Accept',
      value: 'b3fxeyclp4hxtcunohlpak2y'
    })
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
