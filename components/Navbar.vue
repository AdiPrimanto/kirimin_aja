<template>
    <nav id="nav" class="nav-wrapper w-full sm:flex min-h-20 sticky top-0 z-20">
        <div
            class="w-full px-28 py-4 mx-auto flex items-center justify-between"
        >
            <div class="pr-5">
                <NuxtLink to="/">
                    <img
                        src="/images/svg-logo-primary.svg"
                        alt="logo"
                        class="w-40"
                    />
                </NuxtLink>
            </div>
            <ul class="flex items-center flex-col md:flex-col lg:flex-row">
                <li class="relative">
                    <nuxt-link
                        class="text-black font-medium hover:text-purple-300 text-base px-4 py-3"
                        to="/"
                    >
                        Beranda
                    </nuxt-link>
                </li>
                <li class="relative">
                    <nuxt-link
                        class="text-black font-medium hover:text-purple-300 text-base px-4 py-3"
                        to="/"
                        >Blog</nuxt-link
                    >
                </li>
                <li class="relative">
                    <nuxt-link
                        class="text-black font-medium hover:text-purple-300 text-base px-4 py-3"
                        to="/"
                        >Kabar</nuxt-link
                    >
                </li>
                <li class="relative">
                    <a
                        class="text-black font-medium hover:text-purple-300 text-base px-4 py-3 flex gap-2 items-baseline cursor-pointer select-none"
                        @click="showDropdown()"
                    >
                        <span>Layanan</span>
                        <img src="/chevron-bottom.svg" class="w-3 h-3" alt="" />
                    </a>
                    <div class="block relative z-50">
                        <ul
                            :class="{ hidden: dropdownMenu === false }"
                            class="absolute text-gray-700 pd-3 bg-white w-96 rounded-lg shadow-xl"
                        >
                            <li class="p-3 text-sm">
                                <nuxt-link
                                    class="p-2 link-hover rounded whitespace-no-wrap flex gap-3 items-center"
                                    to="/"
                                >
                                    <div>
                                        <img
                                            src="/manajemen-order.svg"
                                            class="w-6 h6"
                                            alt=""
                                        />
                                    </div>
                                    <div class="flex flex-col">
                                        <span
                                            class="font-medium hover:text-[#6f2fab]"
                                        >
                                            Manajemen Order
                                        </span>
                                        <span class="opacity-70">
                                            Platform management order dengan
                                            multi ekspedisi
                                        </span>
                                    </div>
                                </nuxt-link>
                            </li>
                            <li class="p-3 text-sm">
                                <nuxt-link
                                    class="p-2 link-hover rounded whitespace-no-wrap flex gap-3 items-center"
                                    to="/integrasi-api"
                                >
                                    <div>
                                        <img
                                            src="/integrasi-api.svg"
                                            class="w-6 h6"
                                            alt=""
                                        />
                                    </div>
                                    <div class="flex flex-col">
                                        <span
                                            class="font-medium hover:text-[#6f2fab]"
                                        >
                                            Integrasi API
                                        </span>
                                        <span class="opacity-70">
                                            Hubungkan toko online-mu dengan kami
                                        </span>
                                    </div>
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                </li>
                <li class="relative">
                    <nuxt-link
                        class="text-black font-medium hover:text-purple-300 text-base px-4 py-3"
                        to="/"
                        >Lacak</nuxt-link
                    >
                </li>
                <li class="relative">
                    <div class="vertical-spacer"></div>
                </li>
                <li class="relative">
                    <nuxt-link
                        class="text-black font-medium hover:text-purple-300 text-base px-4 py-3"
                        to="/"
                        >Daftar</nuxt-link
                    >
                </li>
                <li class="relative">
                    <nuxt-link to="/" class="btn-primary"> Masuk </nuxt-link>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            dropdownMenu: false,
        }
    },
    mounted() {
        window.onscroll = function (e) {
            let element = document.getElementById('nav')
            if (
                document.body.scrollTop > 40 ||
                document.documentElement.scrollTop > 40
            ) {
                element.classList.remove('nav-wrapper', 'shadow-md')
                element.classList.add('bg-white', 'shadow-md')
            } else {
                element.classList.add('nav-wrapper', 'shadow-md')
                element.classList.remove('bg-white', 'shadow-md')
            }
        }
    },
    methods: {
        showDropdown: function () {
            this.dropdownMenu === true
                ? (this.dropdownMenu = false)
                : (this.dropdownMenu = true)
        },
    },
}
</script>

<style scoped>
@media screen and (min-width: 1024px) {
    .vertical-spacer {
        margin: 0 1rem;
        width: 2px;
        height: 24px;
        background: #000;
        opacity: 0.5;
    }
}

.link-hover {
    @apply hover:border-purple-primary hover:border-2;
}

.nav-wrapper {
    background: radial-gradient(
        89.87% 80.87% at 89.02% -25.74%,
        #e0cef2 20%,
        transparent 100%,
        transparent 100%
    );
}
/* } */
</style>
