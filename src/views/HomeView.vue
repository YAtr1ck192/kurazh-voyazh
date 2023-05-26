<template>
  <div class="home">
      <statusBlock />
      <promoBlock />
      <historyStroke />
  </div>
</template>

<script>

import statusBlock from "@/components/statusBlock";
import promoBlock from "@/components/promoBlock";
import historyStroke from "@/components/historyStroke";

export default {
  name: 'HomeView',
  components: {
      statusBlock,
      promoBlock,
      historyStroke
  }
}
</script>

<style scoped lang="scss">

</style>
