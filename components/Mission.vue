<template>
    <section class="mb-28 mx-10 md:mx-24 lg:mx-24">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6 mt-16">
            <div class="flex flex-col gap-4">
                <h3 class="text-4xl text-black font-bold text-left">
                    Our Mission
                </h3>
                <ul class="list-none">
                    <li
                        class="rounded-md relative border-2 border-purple-primary bg-[#bb92e140] p-3 pl-11 mb-3 list-check"
                        v-for="(list, index) in lists"
                        :key="index"
                    >
                        {{ list.body }}
                    </li>
                </ul>
            </div>
            <div class="flex flex-col gap-3">
                <p>
                    <span class="text-purple-primary">KiriminAja</span> ebuah
                    platform yang memberikan kemudahan untuk pengiriman paket
                    dan menemukan ekspedisi sesuai kebutuhan masyarakat, dengan
                    metode pengiriman COD dan Non-COD yang dikembangkan oleh PT
                    Selalu Siap Solusi.
                </p>
                <p>
                    KiriminAja memberikan solusi untuk UMKM, pebisnis online,
                    serta seluruh masyarakat Indonesia yang ingin melakukan
                    pengiriman paket.
                </p>
                <p>KiriminAja menawarkan:</p>
                <ul class="list-disc pl-4">
                    <li>
                        Kemudahan pengiriman paket dengan pilihan berbagai
                        ekspedisi.
                    </li>
                    <li>
                        Adanya layanan pengiriman COD (Cash On Delivery) dengan
                        pencairan dana harian dan sistem pengambilan paket
                        dirumah oleh ekspedisi.
                    </li>
                    <li>
                        Layanan pengiriman paket non-cod dengan sistem
                        pengambilan paket dirumah oleh ekspedisi.
                    </li>
                    <li>
                        Platform yang dapat membantu pebisnis online
                        mengendalikan dan mengelola bisnisnya dengan lebih baik.
                    </li>
                </ul>
                <p>
                    Dengan layanan dan inovasi yang ditawarkan, KiriminAja
                    memiliki komitmen untuk berkontribusi pada perekonomian
                    Indonesia, dengan cara memberikan solusi serta kemudahan
                    bagi para pebisnis online supaya bisnisnya terus berkembang.
                </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            lists: [
                {
                    body: 'Meningkatkan penjualan produk UMKM secara online.',
                },
                { body: 'Memberikan inovasi-inovasi terbaru dan terbaik.' },
                {
                    body: 'Memberikan pelayanan yang maksimal dan optimal untuk pelanggan.',
                },
                {
                    body: 'Mengenalkan KiriminAja seluas-luasnya ke seluruh Indonesia.',
                },
            ],
        }
    },
    mounted() {},
}
</script>

<style scoped>
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
    left: 0.75rem;
}
</style>
