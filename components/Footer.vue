<template>
    <footer
        class="bg-white mx-10 md:mx-24 lg:mx-24 pt-20 pb-10 text-black text-lg"
    >
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
            <div class="flex flex-col gap-2">
                <img
                    src="/images/svg-logo-primary.svg"
                    class="w-2/4 h-14"
                    alt=""
                />
                <h4 class="text-[#6c757d] text-base">PT. Selalu Siap Solusi</h4>
                <div class="mt-2 flex flex-col gap-2">
                    <div
                        class="flex gap-2"
                        v-for="(contact, index) in contacts"
                        :key="index"
                    >
                        <img :src="contact.img" class="w-6 h-6" alt="" />
                        <p class="text-[#6c757d] opacity-70 text-base">
                            {{ contact.body }}
                        </p>
                    </div>
                </div>
                <h4 class="text-[#6c757d] text-base mt-2">Terdaftar di</h4>
                <img
                    src="https://kiriminaja.com/assets/home-2/logo-kominfo.svg"
                    class="w-1/4 h-10"
                    alt="Penyelenggara Sertifikasi Elektronik"
                />
            </div>
            <div>&nbsp;</div>
            <div class="flex flex-col gap-2">
                <h4 class="text-[#6c757d] text-base">Tautan Cepat</h4>
                <ul class="list-none">
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/">Cek Tarif Aja</NuxtLink>
                    </li>
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/">Kabar Buatmu</NuxtLink>
                    </li>
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/">Manajemen Order</NuxtLink>
                    </li>
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/integrasi-api">Integrasi API</NuxtLink>
                    </li>
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/">
                            Karir
                            <span
                                class="bg-[#a26ad640] text-[#a26ad6] text-xs font-medium p-1 rounded-full"
                            >
                                We're Hiring!
                            </span>
                        </NuxtLink>
                    </li>
                </ul>
            </div>
            <div class="flex flex-col gap-2">
                <h4 class="text-[#6c757d] text-base">KiriminAja</h4>
                <ul class="list-none">
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/about">Tentang Kami</NuxtLink>
                    </li>
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/">Syarat & Ketentuan</NuxtLink>
                    </li>
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/">Kebijakan Privasi</NuxtLink>
                    </li>
                    <li
                        class="text-[#333333] text-base mb-2 hover:text-purple-300"
                    >
                        <NuxtLink to="/">Fakta & Pertanyaan</NuxtLink>
                    </li>
                </ul>
            </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-4 mt-8">
            <p class="text-[#6c757d] text-base mb-0">
                Copyright © 2022
                <a
                    href="https://kiriminaja.com"
                    aria-current="page"
                    class="font-medium text-[#333333] hover:text-purple-300"
                    >KiriminAja.com</a
                >
                . All rights reserved.
            </p>

            <div class="flex justify-end gap-4">
                <div v-for="(sosmed, index) in sosmeds" :key="index">
                    <NuxtLink :to="sosmed.href">
                        <img :src="sosmed.img" class="w-6 h-6" alt="" />
                    </NuxtLink>
                </div>

                <div
                    class="flex gap-1 items-center bg-[#f0f0f0] pt-1 px-6 rounded-full"
                >
                    <span class="text-xs">Dark</span>
                    <button
                        class="w-10 h-5 p-0.5 rounded-full bg-purple-primary"
                        @click="toggleDarkTheme()"
                    >
                        <div
                            class="w-4 h-4 bg-white rounded-full dark:bg-gray-800 translate-x-5 transition-all"
                        ></div>
                    </button>
                    <span class="text-xs">Light</span>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            contacts: [
                {
                    img: '/location.svg',
                    body: 'Jl. Palagan Tentara Pelajar No. 30 KM 08, Mudal, Kelurahan Sariharjo, Kecamatan Ngaglik, Kabupaten Sleman, Provinsi Daerah Istimewa Yogyakarta',
                },
                {
                    img: '/email.svg',
                    body: 'support@kiriminaja.com',
                },
                {
                    img: '/phone.svg',
                    body: '0274 8000 123',
                },
            ],
            sosmeds: [
                { img: '/tiktok.svg', href: '/' },
                { img: '/facebook.svg', href: '/' },
                { img: '/instagram.svg', href: '/' },
                { img: '/linkedin.svg', href: '/' },
                { img: '/youtube.svg', href: '/' },
            ],
            theme: 'light',
        }
    },
    mounted() {
        localStorage.setItem('theme', 'light')
        if (localStorage.getItem('theme') === 'dark') {
            document.documentElement.classList.add('dark')
        }
    },
    methods: {
        toggleDarkTheme: function () {
            console.log('object')
            if (localStorage.getItem('theme') === 'dark') {
                localStorage.setItem('theme', 'light')
                document.documentElement.classList.remove('dark')
            } else {
                localStorage.setItem('theme', 'dark')
                document.documentElement.classList.add('dark')
            }
        },
    },
}
</script>
