<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    name: 'CHARACTERS',
                    href: '/CHARACTERS',
                    active: false
                },
                {
                    name: 'COMICS',
                    href: '/COMICS',
                    active: false
                },
                {
                    name: 'MOVIES',
                    href: '/MOVIES',
                    active: false
                },
                {
                    name: 'TV',
                    href: '/TV',
                    active: false
                },
                {
                    name: 'GAMES',
                    href: '/GAMES',
                    active: false
                },
                {
                    name: 'COLLECTIBLES',
                    href: '/COLLECTIBLES',
                    active: false
                },
                {
                    name: 'VIDEOS',
                    href: '/VIDEOS',
                    active: false
                },
                {
                    name: 'FANS',
                    href: '/FANS',
                    active: false
                },
                {
                    name: 'NEWS',
                    href: '/NEWS',
                    active: false
                },
                {
                    name: 'SHOP',
                    href: '/SHOP',
                    active: false
                },
            ],
        }
    }
}
</script>

<template>
    <header>
        <div class="container flex">

            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>

            <nav class="nav-link">
                <ul class="flex">
                    <li v-for="(link, index) in links" :key="index">
                        {{ link.name }}</li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    padding: 1rem 0;

    .container {
        align-items: center;
    }

    .logo {
        width: 20%;
    }

    .nav-link {
        width: 80%;


        ul {
            column-gap: 1rem;
            justify-content: end;
        }
    }
}
</style>