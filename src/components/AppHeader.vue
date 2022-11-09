<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    name: 'CHARACTERS',
                    href: '/characters',
                    active: false
                },
                {
                    name: 'COMICS',
                    href: '/comics',
                    active: true
                },
                {
                    name: 'MOVIES',
                    href: '/movies',
                    active: false
                },
                {
                    name: 'TV',
                    href: '/tv',
                    active: false
                },
                {
                    name: 'GAMES',
                    href: '/games',
                    active: false
                },
                {
                    name: 'COLLECTIBLES',
                    href: '/collectibles',
                    active: false
                },
                {
                    name: 'VIDEOS',
                    href: '/videos',
                    active: false
                },
                {
                    name: 'FANS',
                    href: '/fans',
                    active: false
                },
                {
                    name: 'NEWS',
                    href: '/new',
                    active: false
                },
                {
                    name: 'SHOP',
                    href: '/shop',
                    active: false
                },
            ],
        }
    },
    methods: {
        setActive(index) {

            this.links.forEach(element => {
                element.active = false
            });

            this.links[index].active = true
        }
    }
}
</script>

<template>
    <header>
        <div class="container flex">

            <div class="logo">
                <a href="">
                    <img src="../assets/img/dc-logo.png" alt="comics dc">
                </a>
            </div>

            <nav class="nav-link">
                <ul class="flex">
                    <li v-for="(link, index) in links" :class="{ 'active': link.active }"
                        @click.prevent="setActive(index)">
                        <a :href="link.href">{{ link.name }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

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
            column-gap: 1.5rem;
            justify-content: end;

            a {
                font-size: 0.8rem;
                font-weight: bold;
            }

            li.active {
                position: relative;
                color: $primary-color;
            }

            li.active::after {
                content: "";
                position: absolute;
                left: 0;
                top: 73px;
                width: 100%;
                height: 6px;
                background-color: $primary-color;
            }
        }
    }
}
</style>