<template>
    <header class="my-12 mx-10 md:mx-24 lg:mx-24">
        <div class="swiper swiper-banner">
            <div class="swiper-wrapper">
                <div
                    v-for="(sliderBanner, index) in sliderBanners"
                    :key="index"
                    class="swiper-slide"
                    :class="`slide--1`"
                >
                    <div class="slider-content">
                        <div
                            class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8"
                        >
                            <img
                                :src="sliderBanner.image"
                                class="h-96"
                                alt=""
                            />
                            <div class="p-4">
                                <span
                                    class="bg-[#f767071A] text-[#f76707] text-sm font-medium p-2 rounded-full"
                                >
                                    #{{ sliderBanner.id }} Info
                                </span>
                                <h2 class="text-4xl text-black font-bold mt-4">
                                    {{ sliderBanner.title }}
                                </h2>
                                <p class="text-xl text-black opacity-70 mt-4">
                                    {{ sliderBanner.description }}
                                </p>
                                <template v-if="sliderBanner.lists.length > 0">
                                    <ul class="list-none mt-4">
                                        <li
                                            class="relative pl-6 mb-3 list-check"
                                            v-for="(
                                                list, idx
                                            ) in sliderBanner.lists"
                                            :key="idx"
                                        >
                                            {{ list.info }}
                                        </li>
                                    </ul>
                                </template>
                                <div class="mt-8">
                                    <a href="/" class="btn-primary">
                                        Selengkapnya
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- If pagination is needed -->
            <div class="swiper-pagination"></div>

            <!-- If navigation buttons are needed -->
            <!-- <div class="swiper-button-prev"></div>
            <div class="swiper-button-next"></div> -->
        </div>
    </header>
</template>

<script>
import { Swiper, Navigation, Pagination, Autoplay } from 'swiper'
import 'swiper/swiper-bundle.min.css'

export default {
    data() {
        return {}
    },
    computed: {
        sliderBanners() {
            return this.$store.state.sliderBanners
        },
    },
    mounted() {
        // add or remove unused modules
        Swiper.use([Navigation, Pagination, Autoplay])

        // init Swiper:
        const swiper = new Swiper('.swiper-banner', {
            // Optional parameters
            // @see https://swiperjs.com/swiper-api#parameters
            direction: 'horizontal',
            loop: true,
            // remove unused modules if needed
            modules: [Navigation, Pagination, Autoplay],

            // Pagination if needed
            pagination: {
                el: '.swiper-pagination',
                type: 'bullets',
                clickable: true,
            },
            // Autoplay if needed
            autoplay: {
                delay: 3000,
            },
            // Navigation arrows if needed
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },
        })
    },
}
</script>

<style scoped>
.swiper {
    height: 100%;
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
.swiper-pagination {
    position: initial !important;
}
.slider-content {
    color: #000;
}
.slide--1 {
    background-color: transparent;
}
.list-check::before {
    content: '';
    display: block;
    width: 20px;
    height: 20px;
    background-image: url(https://kiriminaja.com/assets/home-2/shape.svg);
    background-size: 20px;
    border-radius: 50%;
    position: absolute;
    top: calc(50% - 10px);
    left: 0;
}
</style>
