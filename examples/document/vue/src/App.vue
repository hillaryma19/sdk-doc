<template>
  <div id="app">
  </div>
</template>

<script>
const Editor = window.shimo.sdk.document.Editor
const editor = new Editor()

export default {
  name: 'app',
  mounted: () => {
    editor.render(document.querySelector('#app'))
  }
}
</script>

<style>
html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
