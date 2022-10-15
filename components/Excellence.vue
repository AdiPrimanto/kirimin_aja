<template>
    <section class="mb-28 mx-10 md:mx-24 lg:mx-24">
        <h3 class="text-4xl text-black font-bold text-center">
            Untuk Semua Kebutuhan Pengiriman Paketmu
        </h3>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-16">
            <div
                class="flex flex-col rounded-xl shadow-md"
                v-for="(packet, id) in packets"
                :key="id"
            >
                <div class="block mt-3 relative">
                    <div class="px-4 py-2 with-accent">
                        <div
                            class="inline-block p-2 p-lg-3 rounded-full bg-purple-primary text-purple-primary bg-opacity-10"
                        >
                            <img :src="packet.img" alt="" />
                        </div>
                    </div>
                </div>
                <div class="p-4">
                    <span class="text-2xl text-black font-bold">
                        {{ packet.title }}
                    </span>
                    <p class="text-base text-black opacity-50 mt-2">
                        {{ packet.body }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            packets: [
                {
                    id: 1,
                    img: '/images/kebutuhan-pengiriman/layanan-terintegrasi.svg',
                    title: 'Layanan Terintegrasi',
                    body: 'Dashboard, API, Dan Mobile kami sediakan untuk mengontrol & monitoring lebih mudah.',
                },
                {
                    id: 2,
                    img: '/images/kebutuhan-pengiriman/ekspedisi-terbaik.svg',
                    title: 'Ekspedisi Terbaik',
                    body: 'Kamu bisa pilih layanan sameday, next day, reguler, ekonomi, kargo dan lainya sesukamu.',
                },
                {
                    id: 3,
                    img: '/images/kebutuhan-pengiriman/sistem-otomatis.svg',
                    title: 'Sistem Otomatis',
                    body: 'Cetak resi / AWB, tracking, saldo COD dan banyak fitur lainnya.',
                },
                {
                    id: 4,
                    img: '/images/kebutuhan-pengiriman/selalu-ada.svg',
                    title: 'Selalu Ada Untukmu',
                    body: 'Kami selalu ada tanpa libur 24 Jam non stop, dan pihak ekpedisi.',
                },
                {
                    id: 5,
                    img: '/images/kebutuhan-pengiriman/laporan-aktual.svg',
                    title: 'Laporan Aktual',
                    body: 'Kemudahan pantau paket, pencairan COD, saldo, semuanya.',
                },
                {
                    id: 6,
                    img: '/images/kebutuhan-pengiriman/friendly.svg',
                    title: 'Friendly',
                    body: 'Ciptakan solusi terbaik dengan masukan, kritik, dan diskusi.',
                },
            ],
        }
    },
    mounted() {},
}
</script>

<style scoped>
.with-accent::before {
    position: absolute;
    left: -1px;
    width: 4px;
    border-radius: 0 20px 20px 0;
    top: 0;
    height: 100%;
    background: #6f2fab;
    content: '';
}
</style>
