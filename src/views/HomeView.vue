<template>
  <div class="home">
      <statusBlock />
      <promoBlock />
      <historyStroke id="historyStroke"/>
      <categoriesMenu />
      <div class="container">
          <bigMenuCard />
      </div>
  </div>
</template>

<script>

import statusBlock from "@/components/statusBlock";
import promoBlock from "@/components/promoBlock";
import historyStroke from "@/components/historyStroke";
import categoriesMenu from "@/components/categoriesMenu";
import bigMenuCard from "@/components/menu/bigMenuCard";

export default {
  name: 'HomeView',
  components: {
      statusBlock,
      promoBlock,
      historyStroke,
      categoriesMenu,
      bigMenuCard
  }
}
</script>

<style scoped lang="scss">
    #historyStroke {
        margin-bottom: 20px;
    }
</style>
