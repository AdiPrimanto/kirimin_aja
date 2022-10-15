<template>
    <section class="my-12 mx-10 md:mx-24 lg:mx-24">
        <div class="swiper swiper-courier">
            <div class="swiper-wrapper">
                <div
                    class="swiper-slide p-4"
                    v-for="(courier, index) in couriers"
                    :key="index"
                >
                    <img :src="courier.img" class="max-h-12 w-auto" alt="" />
                </div>
            </div>
            <!-- Add Pagination -->
            <div class="swiper-pagination"></div>
        </div>
    </section>
</template>

<script>
// import Swiper JS
// add or remove unused modules
import { Swiper, Navigation, Pagination, Autoplay, SwiperSlide } from 'swiper'
import 'swiper/swiper-bundle.min.css'

export default {
    data() {
        return {}
    },
    computed: {
        couriers() {
            return this.$store.state.couriers
        },
    },
    mounted() {
        // add or remove unused modules
        Swiper.use([Navigation, Pagination, Autoplay])

        // init Swiper:
        /* eslint-disable no-unused-vars */
        const swiper = new Swiper('.swiper-courier', {
            // Optional parameters
            // @see https://swiperjs.com/swiper-api#parameters
            direction: 'horizontal',
            slidesPerView: 6,
            spaceBetween: 30,
            // loop: false,
            loop: true,
            // remove unused modules if needed
            modules: [Navigation, Pagination, Autoplay],

            // Pagination if needed
            // pagination: {
            //     el: '.swiper-pagination',
            //     type: 'bullets',
            //     clickable: true,
            // },
            // Autoplay if needed
            autoplay: {
                delay: 3000,
            },
            // Navigation arrows if needed
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },
            // Configure other options. Not tested
        })
    },
}
</script>

<style scoped>
.swiper {
    height: fit-content;
    overflow: hidden;
    position: relative;
    width: 100%;
    /* width: 500px; */
}
.swiper-slide {
    align-items: center;
    display: flex;
    justify-content: center;
}
.slider-content {
    color: #000;
}
.slide--1 {
    background-color: #fff;
}
</style>
