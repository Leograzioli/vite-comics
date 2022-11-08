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

    background-color: black;
    color: white;

    .container {
        padding: 3rem 0;
    }
}
</style>