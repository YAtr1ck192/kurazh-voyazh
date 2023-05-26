<template>
  <div class="home">
      <statusBlock />
      <promoBlock />
  </div>
</template>

<script>

import statusBlock from "@/components/statusBlock";
import promoBlock from "@/components/promoBlock";

export default {
  name: 'HomeView',
  components: {
      statusBlock,
      promoBlock
  }
}
</script>

<style scoped lang="scss">

</style>
