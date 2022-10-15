<template>
    <section class="py-28 mx-10 md:mx-24 lg:mx-24">
        <div class="flex flex-col gap-3">
            <h3 class="text-4xl text-black font-bold text-center">
                Dipercayai oleh
            </h3>
            <p class="font-medium text-center">
                KirimiAja berkomitmen untuk selalu mendukung perkembangan dan
                kemajuan UMKM di seluruh Indonesia
            </p>

            <div
                class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-6 gap-4 mt-14 px-32"
            >
                <div
                    class="flex flex-col justify-center items-center gap-2"
                    v-for="(logo, id) in logos"
                    :key="id"
                >
                    <img :src="logo.img" class="w-auto" alt="" />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            logos: [
                {
                    id: '1',
                    img: 'https://kiriminaja.com/assets/atrust/client-arcelle-2.png',
                },
                {
                    id: '2',
                    img: 'https://kiriminaja.com/assets/home-2/blanja24.png',
                },
                {
                    id: '3',
                    img: 'https://kiriminaja.com/assets/atrust/client-bakpia.png',
                },
                {
                    id: '4',
                    img: 'https://kiriminaja.com/assets/atrust/logo_dion_farma.png',
                },
                {
                    id: '5',
                    img: '	https://kiriminaja.com/assets/atrust/logo_natasha.png',
                },
                {
                    id: '6',
                    img: 'https://kiriminaja.com/assets/atrust/logo_paeko.png',
                },
                {
                    id: '7',
                    img: 'https://kiriminaja.com/assets/atrust/client-diy.png',
                },
                {
                    id: '8',
                    img: 'https://kiriminaja.com/assets/atrust/client-nimco.png',
                },
                {
                    id: '9',
                    img: 'https://kiriminaja.com/assets/atrust/client-finna-1.png',
                },
                {
                    id: '10',
                    img: '	https://kiriminaja.com/assets/atrust/client-sibakul.png',
                },
                {
                    id: '11',
                    img: 'https://kiriminaja.com/assets/atrust/client-clandys.png',
                },
                {
                    id: '12',
                    img: 'https://kiriminaja.com/assets/atrust/client-hayyana-1.png',
                },
                {
                    id: '13',
                    img: '',
                },
                {
                    id: '14',
                    img: 'https://kiriminaja.com/assets/atrust/efes-efes.png',
                },
                {
                    id: '15',
                    img: 'https://kiriminaja.com/assets/atrust/client-yukbid-2.png',
                },
                {
                    id: '16',
                    img: 'https://kiriminaja.com/assets/atrust/client-misseana.png',
                },
                {
                    id: '17',
                    img: 'https://kiriminaja.com/assets/atrust/client-inolabs-1.png',
                },
                {
                    id: '18',
                    img: '',
                },
            ],
        }
    },
    mounted() {},
}
</script>

<style scoped></style>
