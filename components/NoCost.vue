<template>
    <section class="pt-28 mx-10 md:mx-24 lg:mx-24">
        <div class="flex flex-col gap-3">
            <h3 class="text-4xl text-black font-bold text-center">
                Tanpa Biaya Apapun
            </h3>
            <p class="font-medium text-center">
                Sebuah solusi optimal sehingga Anda tidak perlu pusing lagi
                memikirkan biaya berlangganan API
            </p>

            <div class="w-full md:w-32/6 lg:w-3/6 px-32 relative mt-20 mx-auto">
                <div class="card selected">
                    <div
                        class="card-header border-0 bg-transparent text-center relative"
                    >
                        <div class="mb-4 text-secondary">
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                class="mx-auto"
                                width="28"
                                height="28"
                                viewBox="0 0 24 24"
                                stroke-width="2"
                                stroke="currentColor"
                                fill="currentColor"
                                fill-opacity="0.5"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                            >
                                <path
                                    stroke="none"
                                    d="M0 0h24v24H0z"
                                    fill="none"
                                ></path>
                                <path
                                    d="M12 12c2 -2.96 0 -7 -1 -8c0 3.038 -1.773 4.741 -3 6c-1.226 1.26 -2 3.24 -2 5a6 6 0 1 0 12 0c0 -1.532 -1.056 -3.94 -2 -5c-1.786 3 -2.791 3 -4 2z"
                                ></path>
                            </svg>
                            <h4 class="font-bold">Freemium</h4>
                        </div>
                        <a
                            class="btn btn-secondary text-white border-2 mb-2 full-radius inline-block"
                            href="https://wa.me/6285975255552"
                            target="_blank"
                        >
                            Hubungi Kami
                        </a>
                        <div class="absolute mt-4 annualy pb-4 px-4 pt-4">
                            <div class="text-base">
                                Solusi tepat untuk pertumbuhan bisnis yang
                                signifikan
                            </div>
                        </div>
                    </div>
                    <div
                        class="card-body border-top border-light-2 m-2 p-lg-4 z-10 relative"
                    >
                        <small>Integration includes</small>
                        <ul class="my-2 p-0 relative">
                            <li>Cashback Ongkir Up 25%</li>
                            <li>Unlimited API call per harinya</li>
                            <li>
                                Pengiriman cod, reguler, next day, dan instant
                            </li>
                            <li>Dukungan penuh via email dan sosial media</li>
                            <li>Pembuatan label pengiriman otomatis</li>
                            <li>Laporan order pengiriman</li>
                        </ul>
                        <a
                            class="btn btn-secondary text-white border-2 w-100 mt-2 full-radius block"
                            href="https://wa.me/6285975255552"
                            target="_blank"
                            >Ajukan Sekarang</a
                        >
                    </div>
                </div>
            </div>
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
.card {
    position: relative;
    display: flex;
    flex-direction: column;
    min-width: 0;
    word-wrap: break-word;
    border-radius: 0.75rem;
}
.card.selected {
    background: linear-gradient(to bottom, #f76707, rgba(247, 103, 7, 0.25));
    border: none;
    padding: 2px;
}
.card.selected::before {
    content: '';
    position: absolute;
    margin: 4px 4px;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    border-radius: 0.6rem;
    background: #fff;
    z-index: 0;
}
.card.selected .card-header {
    overflow: hidden;
}
.card-header:first-child {
    border-radius: calc(0.75rem - 2px) calc(0.75rem - 2px) 0 0;
}
.card-header {
    padding-top: 3.5rem;
    padding-bottom: 6.5rem;
}
.bg-transparent {
    background-color: transparent !important;
}
.card.selected .card-header::before {
    content: '';
    height: 400px;
    top: -205px;
    border-radius: 0 0 100% 100%;
    position: absolute;
    left: -140px;
    right: -140px;
    border-bottom: 4px solid #f76707;
}
.text-secondary {
    color: #f76707;
}
.card-header .annualy {
    left: 0;
    bottom: 0;
    right: 0;
}
.card-body {
    flex: 1 1 auto;
    padding: 1rem 1rem;
}
.card ul li {
    padding-left: 1.75rem;
}
.card ul li::before {
    content: '';
    width: 0.7rem;
    height: 0.7rem;
    border: 2px solid #f76707;
    border-radius: 100%;
    position: absolute;
    left: 0;
    margin-top: 6px;
}
.border-light-2 {
    border-color: #eee !important;
}
.border-top {
    border-top: 1px solid #dee2e6 !important;
}
</style>
