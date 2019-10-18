<template>
  <div id="app">
    <Sidenav/>
    <Content/>
  </div>
</template>

<script>
import Sidenav from '@/components/Sidenav'
import Content from '@/components/Content'
export default {
  name: 'app',
  components: {
    Sidenav,
    Content
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Segoe UI;
  // background: #FBFBFB;
}

#app {
  display: grid;
  grid-template-columns: 380px 1204px;
}
</style>
