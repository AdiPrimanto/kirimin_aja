<template>
    <section class="py-28 bg-[#F8F9FA]">
        <div class="mx-10 md:mx-24 lg:mx-24">
            <h3 class="text-4xl text-black font-bold text-center">
                Kurir Terhubung
            </h3>
            <p class="font-medium text-center">
                KiriminAJA selalu terhubung dengan expedisi yang terbaik di
                Indonesia, dan akan terus bertambah lagi
            </p>

            <div
                class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 mt-16 px-32"
            >
                <div
                    class="flex flex-col gap-3 items-center justify-center"
                    v-for="(packet, id) in packets"
                    :key="id"
                >
                    <img :src="packet.img" class="h-14 w-auto" alt="" />
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
                    img: '/images/courier/anteraja.png',
                },
                {
                    id: 2,
                    img: '/images/courier/jne.png',
                },
                {
                    id: 3,
                    img: '/images/courier/jnt.png',
                },
                {
                    id: 4,
                    img: '/images/courier/ncs.png',
                },
                {
                    id: 5,
                    img: '/images/courier/sap.png',
                },
                {
                    id: 6,
                    img: '/images/courier/sicepat.png',
                },
                {
                    id: 7,
                    img: '/images/courier/sentral.png',
                },
                {
                    id: 8,
                    img: '/images/courier/idexpress.png',
                },
            ],
        }
    },
    mounted() {},
}
</script>

<style scoped></style>
