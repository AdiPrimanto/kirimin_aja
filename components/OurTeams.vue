<template>
    <section class="mb-28 mx-10 md:mx-24 lg:mx-24">
        <h3 class="text-4xl text-black font-bold text-center">Our Teams</h3>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-3 mt-16">
            <div
                class="flex flex-col rounded-xl p-2"
                v-for="(team, id) in ourTeams"
                :key="id"
            >
                <img :src="team.img" class="rounded-md" alt="" />
                <div class="mt-2">
                    <span class="text-xl text-black font-bold">
                        {{ team.title }}
                    </span>
                    <p class="text-sm text-black opacity-80">
                        {{ team.body }}
                    </p>
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
    computed: {
        ourTeams() {
            return this.$store.state.ourTeams
        },
    },
    mounted() {},
}
</script>

<style scoped></style>
