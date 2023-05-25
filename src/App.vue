<template>
  <div id="app">
      <headerBlock />
      <router-view> </router-view>

  </div>
</template>

<script>
import headerBlock from "./components/headerBlock"
export default {
    name: 'App',
    components: {
        headerBlock,
    }
}
</script>

<style lang="scss">
    @import "src/assets/styles/global";
</style>
