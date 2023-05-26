<template>
    <div class="menuCard">
        <img src="/img/small-card-img-1.png" alt="small-card-img" class="card-img">
        <div class="card-content">
            <div class="top-and-middle-items">
                <div class="items-in-top">
                    <h3 class="title">Чипсы, 50гр</h3>
                    <router-link to="/" class="food-info-icon">
                        <img src="/img/food-info-icon.png" alt="food-info-icon">
                    </router-link>
                </div>
                <div class="card-desc">Вкус: соль</div>
            </div>
            <div class="items-in-bottom">
                <div class="card-price">120 ₽</div>
                <button class="on-cart">
                    <img src="/img/status-block-cart.png" alt="status-block-cart" class="cart-img">
                    <div class="cart-text">В заказ</div>
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "smallMenuCard"
}
</script>

<style scoped lang="scss">
    @import "src/assets/styles/global";

    .menuCard {
        width: 310px;
        height: 420px;
        border-radius: 20px;
        background: white;
        box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
        margin-bottom: 100px;

        .card-img {
            width: 100%;
            height: 242px;
        }
        .card-content {
            padding: 15px;
            height: 178px;
            width: 100%;
            display: flex;
            justify-content: space-between;
            flex-direction: column;

            .top-and-middle-items {
                .items-in-top {
                    display: flex;
                    align-items: center;
                    justify-content: space-between;

                    .title {
                        @include inter-600;
                        font-size: 18px;
                        line-height: 23px;
                        max-width: 260px;
                    }
                    .food-info-icon {
                        width: 14px;
                        height: 14px;

                        img {
                            @extend .food-info-icon;
                        }
                    }
                }
                .card-desc {
                    margin-top: 7px;
                    max-height: 34px;
                    @include inter-400;
                    font-size: 14px;
                    line-height: 17px;
                    color: #0E254B99;
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
                .on-cart {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    background: #FF6B17;
                    border-radius: 50px;
                    padding: 8px 30px;
                    border: none;
                    cursor: pointer;

                    .cart-img {
                        margin-right: 9px;
                        width: 20px;
                        height: 20px;
                    }
                    .cart-text {
                        @include inter-600;
                        font-size: 16px;
                        line-height: 20px;
                        color: white;
                    }
                }
            }
        }
    }
</style>
