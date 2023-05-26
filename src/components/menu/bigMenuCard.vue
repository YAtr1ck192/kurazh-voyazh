<template>
    <div class="bigMenuCard">
        <div class="card-images">
            <img src="/img/big-card-img-1-1.png" alt="big-card-img" class="card-img">
            <img src="/img/big-card-img-1-2.png" alt="big-card-img" class="card-img">
        </div>
        <div class="card-content">
            <div class="top-and-middle-items">
                <div class="items-in-top">
                    <div class="title-and-chip">
                        <div class="chip">
                            Набор
                        </div>
                        <h3 class="title">Набор для двоих, 580гр</h3>
                    </div>
                    <router-link to="/" class="food-info-icon">
                        <img src="/img/food-info-icon.png" alt="food-info-icon">
                    </router-link>
                </div>
                <div class="info-about-kit">
                    <img src="/img/kit-info-icon.png" alt="kit-info-icon" class="info-about-kit-icon">
                    <div>На 2 персоны</div>
                </div>
                <div class="card-desc">Багет, ржанная чиабатта, вафли, гриссини, мусс из цветной капусты с беконом, паштет с вишневым конфи, ассорти сыров и мясных</div>
            </div>
            <div class="items-in-bottom">
                <div class="card-price">2375 ₽</div>
                <cartButton />
            </div>
        </div>
    </div>
</template>

<script>
import cartButton from "@/components/cartButton";
export default {
    name: "bigMenuCard",
    components: {
        cartButton
    }
}
</script>

<style scoped lang="scss">
@import "src/assets/styles/global";
.bigMenuCard {
    width: 640px;
    height: 420px;
    border-radius: 20px;
    background: white;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 100px;

    .card-images {
        display: flex;
        align-items: center;
        justify-content: space-between;

        .card-img {
            max-width: 317px;
            width: 100%;
            height: 200px;

            &:first-child {
                border-radius: 20px 0 0 20px;
            }
            &:last-child {
                border-radius: 0 20px 20px 0;
            }
        }
    }
    .card-content {
        padding: 15px;
        height: 220px;
        width: 100%;
        display: flex;
        justify-content: space-between;
        flex-direction: column;

        .top-and-middle-items {
            .items-in-top {
                display: flex;
                align-items: center;
                justify-content: space-between;

                .title-and-chip {
                    display: flex;
                    align-items: center;
                    margin-bottom: 10px;

                    .chip {
                        background: #D5E5FB;
                        border-radius: 34px;
                        color: #3485FF;
                        padding: 2px 13px;
                        @include inter-600;
                        font-size: 18px;
                        line-height: 23px;
                        cursor: pointer;
                    }
                    .title {
                        @include inter-600;
                        font-size: 18px;
                        line-height: 23px;
                        max-width: 260px;
                        margin-left: 7px;
                    }
                }
                .food-info-icon {
                    width: 14px;
                    height: 14px;

                    img {
                        @extend .food-info-icon;
                    }
                }
            }
            .info-about-kit {
                display: flex;
                align-items: center;

                .info-about-kit-icon {
                    width: 20px;
                    height: 20px;
                    margin-right: 10px;
                }
                div {
                    @include inter-400;
                    font-size: 14px;
                    line-height: 17px;
                    color: #0E254B;

                }
            }
            .card-desc {
                max-width: 486px;
                @include card-desc;
            }
        }

        .items-in-bottom {
            display: flex;
            justify-content: space-between;
            align-items: center;

            .card-price {
                @include mont-700;
                font-size: 22px;
                line-height: 27px;
                color: #3485FF;
            }

        }
    }
}
</style>
