<template>
    <div class="container">
        <div class="categories-menu-content">
            <section class="categories-menu-chips">
                <router-link to="/" class="categories-menu-chip">Роллы</router-link>
                <router-link to="/" class="categories-menu-chip">Вино</router-link>
                <router-link to="/" class="categories-menu-chip">Пицца</router-link>
                <router-link to="/" class="categories-menu-chip">Устрицы</router-link>
                <router-link to="/" class="categories-menu-chip">Острое</router-link>
                <router-link to="/" class="categories-menu-chip">Новинки</router-link>
            </section>
            <div class="menu-search-box">
                <input type="text" class="menu-search-form">
                <button class="search-icon">
                    <img src="/img/categoriesMenu-search-icon.png" alt="categoriesMenu-search-icon">
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "categoriesMenu"
}
</script>

<style scoped lang="scss">
    @import "src/assets/styles/global";
    .categories-menu-content {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 10px 0 25px;

        .categories-menu-chips {
            display: flex;
            align-items: center;

            .categories-menu-chip {
                padding: 7px 15px;
                background: #F4F6F9;
                border-radius: 50px;
                margin-right: 12px;
                font-size: 16px;
                line-height: 20px;
                @include inter-400;
                text-decoration: none;
                color: #0E254B99;

                &:hover {
                    color: #0E254B;
                    background: #D5E5FB;
                }
            }
        }
        .menu-search-box {
            display: flex;
            align-items: center;
            position: relative;

            .menu-search-form {
                width: 665px;
                height: 34px;
                border-radius: 30px;
                border: solid 1px #F4F6F9;
                padding: 0 42px 0 10px;
                outline-color: #F4F6F9;
                @include inter-400;
                font-size: 16px;
                line-height: 20px;
                color: #0E254B;
            }
            .search-icon {
                position: absolute;
                right: 10px;
                border: none;
                background: transparent;
                cursor: pointer;
                max-width: 32px;
                max-height: 32px;
            }
        }
    }
</style>
