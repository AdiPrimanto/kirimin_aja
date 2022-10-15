<template>
    <div class="main-wrapper">
        <Navbar />
        <main class="container mx-auto">
            <Slider />
            <Search />
            <Courier />
            <Banner />
            <Excellence />
            <Explore />
            <GetApp />
        </main>
        <Footer />
    </div>
</template>

<script>
export default {
    name: 'IndexPage',
}
</script>

<style>
.main-wrapper {
    background: radial-gradient(
        89.87% 80.87% at 89.02% -25.74%,
        #e0cef2 20%,
        transparent 100%,
        transparent 100%
    );
}
</style>
