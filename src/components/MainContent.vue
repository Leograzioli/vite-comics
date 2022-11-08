<script>
import AppShop from './AppShop.vue';

export default {
    name: "MainContent",
    data() {
        return {};
    },
    components: {
        AppShop
    }
}
</script>

<template>
    <main>
        <div class="container">
            <h2>-- content hoes here -- </h2>
        </div>
        <AppShop />
    </main>
</template>

<style lang="scss" scoped>
main {

    .container {
        padding: 3rem 0;

    }

    // debug
    background-color: black;
    color: white;
}
</style>