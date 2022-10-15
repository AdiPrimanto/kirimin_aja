<template>
    <section class="mt-32 mb-10 mx-10 md:mx-24 lg:mx-24">
        <div
            class="container relative bg-purple-primary overflow-hidden rounded-md"
        >
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6">
                <div class="px-10 z-10">
                    <img
                        src="https://kiriminaja.com/assets/home-2/call-to-action.png"
                        class="w-full"
                        alt=""
                    />
                </div>
                <div class="flex justify-center flex-col gap-3 px-10 z-10">
                    <h2 class="mb-2 text-white text-2xl font-bold">
                        Gratis daftar dalam hitungan detik
                    </h2>
                    <p class="text-white font-medium text-opacity-50 leading-5">
                        Semua bisa mulai kirim paket tanpa ribet. Jadikan
                        pengalaman pengiriman paket lebih mudah dengan
                        KiriminAja.
                    </p>
                    <div class="lg:mt-4">
                        <div class="flex gap-2 w-4/6">
                            <a
                                target="_blank"
                                href="https://apps.apple.com/us/app/kiriminaja/id1544207424"
                            >
                                <img
                                    src="https://kiriminaja.com/assets/service/v2/appstore-compressed.png"
                                    alt=""
                                />
                            </a>
                            <a
                                target="_blank"
                                href="https://play.google.com/store/apps/details?id=id.tries.kiriminaja&amp;hl=in"
                            >
                                <img
                                    src="https://kiriminaja.com/assets/service/v2/googleplay-compressed.png"
                                />
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="img-section"></div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {}
    },
    mounted() {},
}
</script>

<style scoped>
.img-section {
    opacity: 0.5;
    position: absolute;
    left: 0;
    width: 100%;
    top: 0;
    z-index: 0;
    filter: blur(3px);
    height: 100%;
    background-image: url(https://kiriminaja.com/assets/home-2/banner-without-text.png);
    background-size: auto 100%;
    background-position-x: -5rem;
    background-repeat: no-repeat;
}
</style>
