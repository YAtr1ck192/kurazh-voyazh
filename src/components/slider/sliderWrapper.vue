<template>
    <div class="slider-wrapper">
        <swiper class="swiper" :options="swiperOption">
            <swiper-slide
                v-for="(slide, index) in sliderBlockComponents.sliderCards"
                :key="index"
            >
                <sliderCard :value="slide" :slide="slide"/>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>

import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import sliderCard from "@/components/slider/sliderCard";

export default {
    name: "sliderWrapper",
    props: ['sliderBlockComponents'],
    computed: {
        swiperOption() {
            return {
                slidesPerView: 3,
                spaceBetween: 20,
                slidesPerGroup: 1,
                loop: true,

            }
        }
    },
    components: {
        Swiper,
        SwiperSlide,
        sliderCard
    },
}
</script>

<style scoped>

</style>
