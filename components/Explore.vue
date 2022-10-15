<template>
    <section class="mb-28 mx-10 md:mx-24 lg:mx-24">
        <h3 class="text-4xl text-black font-bold text-center">
            Kirim Paket Makin Singkat
        </h3>
        <p class="font-medium text-center mt-2">
            Masih kurang? Yuk explore sekarang biar ngga penasaran
        </p>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6 mt-16">
            <div>
                <img src="/images/info_paket.png" class="w-full" alt="" />
            </div>
            <div>
                <ul class="list-none">
                    <li
                        class="rounded-md relative border-2 p-3 pl-11 mb-3 list-check"
                        v-for="(list, index) in lists"
                        :key="index"
                    >
                        {{ list.body }}
                    </li>
                </ul>
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
                    body: 'Berbagai service expedisi sameday, kargo dan lainnya.',
                },
                { body: 'Penjemputan paket tanpa minimal kiriman.' },
                { body: 'Fitur dropoff atau cashless.' },
                { body: 'Kirim paket COD dengan pencairan tercepat.' },
                { body: 'Platform mudah digunakan (user friendly).' },
                { body: 'Meminimalisir rasio retur.' },
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
