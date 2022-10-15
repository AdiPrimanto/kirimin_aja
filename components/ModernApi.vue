<template>
    <section class="py-28 bg-[#F8F9FA]">
        <div class="mx-10 md:mx-24 lg:mx-24">
            <h3 class="text-4xl text-black font-bold text-center">
                Modern Rest API's, Simply Delivered
            </h3>
            <p class="font-medium text-center">
                Kami menggunakan teknologi REST API terbaru yang lebih mudah
                dimengerti oleh developer ber skala kecil
            </p>

            <div
                class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mt-16"
            >
                <div
                    class="flex flex-col rounded-xl border-2 border-[#eee] bg-white"
                    v-for="(packet, id) in packets"
                    :key="id"
                >
                    <div class="block mt-3 relative">
                        <div class="px-4 pt-2">
                            <div
                                :class="packet.background"
                                class="inline-block p-2 p-lg-3 rounded-full bg-opacity-10"
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
                    img: '/images/modern-api/ongkos-kirim.svg',
                    title: 'Ongkos Kirim Up to Date',
                    body: 'Ongkos kirim langsung dari ekspedisi, tanpa perubahan',
                    background: 'bg-[#ffc10740]',
                },
                {
                    id: 2,
                    img: '/images/modern-api/pickup.svg',
                    title: 'Pickup & Dropoff',
                    body: 'Tentukan dan pilih opsi pengiriman dropoff dan pickup',
                    background: 'bg-[#19875440]',
                },
                {
                    id: 3,
                    img: '/images/modern-api/awb.svg',
                    title: 'AWB Terpusat',
                    body: 'Gak perlu pusing menunggu dapet AWB, kami yang antrikan',
                    background: 'bg-[#dc354540]',
                },
                {
                    id: 4,
                    img: '/images/modern-api/tracking.svg',
                    title: 'Tracking Satu Pintu',
                    body: 'Hasil ekspedisi kami buat dengan satu konsep penyajian',
                    background: 'bg-[#3b599840]',
                },
                {
                    id: 5,
                    img: '/images/modern-api/jangkauan.svg',
                    title: 'Jangkauan Terluas',
                    body: 'Selalu terbuka untuk seluruh area origin dan destinasi',
                    background: 'bg-[#1da1f240]',
                },
                {
                    id: 6,
                    img: '/images/modern-api/selalu-ada.svg',
                    title: 'Selalu Ada',
                    body: 'Selalu terbuka untuk seluruh area origin dan destinasi',
                    background: 'bg-[#d6338440]',
                },
                {
                    id: 7,
                    img: '/images/modern-api/server.svg',
                    title: 'Server Optimal',
                    body: 'Server dapat diakses kapanpun dan dimanapun',
                    background: 'bg-[#ffc10740]',
                },
                {
                    id: 8,
                    img: '/images/modern-api/tim.svg',
                    title: 'Tim teknis friendly',
                    body: 'Ngga perlu worry untuk bertanya tentang teknis',
                    background: 'bg-[#0dcaf040]',
                },
            ],
        }
    },
    mounted() {},
}
</script>

<style scoped></style>
