<template>
  <div id="app">
      <headerBlock />
      <router-view />
      <footerBlock />
  </div>
</template>

<script>

import headerBlock from "./components/headerBlock"
import footerBlock from "@/components/footerBlock";

export default {
    name: 'App',
    components: {
        headerBlock,
        footerBlock
    }
}
</script>

<style lang="scss">
    @import "src/assets/styles/global";
</style>
