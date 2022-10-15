<template>
    <section class="mb-28 mx-10 md:mx-24 lg:mx-24">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6 mt-16">
            <div class="flex flex-col gap-3">
                <h3 class="text-4xl text-black font-bold">
                    Partner Ecosystem & Integrations
                </h3>
                <p class="font-medium">
                    Kami bermitra dengan banyak ekspedisi terkemuka untuk
                    membantu mengembangkan bisnis Anda lebih cerdas, lebih
                    cepat, dan lebih kuat dari sebelumnya.
                </p>
                <ul class="list-none">
                    <li
                        class="rounded-md relative p-1 pl-11 list-check"
                        v-for="(list, index) in lists"
                        :key="index"
                    >
                        {{ list.body }}
                    </li>
                </ul>
                <div class="flex gap-3">
                    <button class="btn-primary">Daftar Gratis!</button>
                    <NuxtLink
                        to="/"
                        class="flex items-center gap-2 font-medium text-purple-primary hover:text-purple-500"
                    >
                        <img src="/partner.svg" class="w-6 h-6" alt="" />
                        Docs
                    </NuxtLink>
                </div>
            </div>

            <div>
                <img
                    src="https://kiriminaja.com/assets/cuate/memory-cuate.svg"
                    class="w-full"
                    alt=""
                />
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            lists: [
                { body: 'Beragam pilihan expedisi & Layanan' },
                { body: 'Support Cash On Delivery' },
                { body: 'Dashboard Monitoring' },
                { body: 'Diskon ongkir dan Cashback ongkir' },
                { body: 'Customer Support Senin - Minggu' },
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
