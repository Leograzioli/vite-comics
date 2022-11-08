<script>
import { getGlobalThis } from '@vue/shared';

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
            currentActive: 1
        }
    },
    methods: {
        setActive(index) {
            this.currentActive = index
            if (this.currentActive === index) {
                this.links.forEach(element => {
                    element.active = false
                });
            }

            this.links[this.currentActive].active = true

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
                    <li v-for="(link, index) in links" :class="{ 'active': link.active }"
                        @click.prevent="setActive(index)">
                        <a href="">{{ link.name }}</a>
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