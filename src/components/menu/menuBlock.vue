<template>
    <div class="container">
        <div class="menu-block-content">
            <div class="item-in-top">
                <div class="logo-and-name-company">
                    <img :src="menuBlockData.logo" alt="menuBlock-company-logo-1" class="company-logo">
                    <h2 class="company-name">{{ menuBlockData.companyName }}</h2>
                </div>
                <div class="chips-about-order">
                    <chipAboutOrder
                        v-for="(chip, index) in menuBlockComponentsData.chips"
                        :key="index"
                        :chip="chip"
                    />
                </div>
            </div>
            <div class="small-cards">
                <smallMenuCard
                    v-for="(smallCard, index) in menuBlockComponentsData.smallCards"
                    :key="index"
                    :smallCard="smallCard"
                />
            </div>
            <div class="big-cards">
                <bigMenuCard
                    v-for="(bigCard, index) in menuBlockComponentsData.bigCards"
                    :key="index"
                    :bigCard="bigCard"
                />
            </div>
            <div class="pagination-block">
                <button class="more">
                    Показать ещё
                </button>
            </div>
        </div>
    </div>
</template>

<script>
import chipAboutOrder from "@/components/menu/chipAboutOrder";
import smallMenuCard from "@/components/menu/smallMenuCard";
import bigMenuCard from "@/components/menu/bigMenuCard";
export default {
    name: "menuBlock",
    props: ['menuBlockData', 'menuBlockComponentsData'],
    components: {
        chipAboutOrder,
        smallMenuCard,
        bigMenuCard
    }
}
</script>

<style scoped lang="scss">
@import "src/assets/styles/global";
.menu-block-content {
    .item-in-top {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 25px;

        .logo-and-name-company {
            @include logo-and-name-company;
        }
        .chips-about-order {
            display: flex;
            align-items: center;
        }
    }
    .small-cards, .big-cards {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 30px;
    }
    .pagination-block {
        display: flex;
        align-items: center;
        justify-content: flex-end;

        .more {
            color: #FF6B17;
            background: #FFE9DC;
            border-radius: 50px;
            border: solid 1px #FF6B1726;
            padding: 9px 30px;
            @include inter-600;
            font-size: 16px;
            line-height: 30px;
            cursor: pointer;
        }
    }
}


</style>
