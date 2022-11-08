<script>
export default {
    name: 'AppShop',
    data() {
        return {
            shopData: [
                {
                    name: 'DIGITAL COMICS',
                    imgName: '-digital-comics',
                    imgType: '.png'
                },
                {
                    name: 'DC MERCHANDISE',
                    imgName: '-merchandise',
                    imgType: '.png'
                },
                {
                    name: 'SUBSCRIPTION',
                    imgName: '-subscriptions',
                    imgType: '.png'
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    imgName: '-shop-locator',
                    imgType: '.png'
                },
                {
                    name: 'DC POWER VISA',
                    imgName: '-power-visa',
                    imgType: '.svg'
                }
            ]
        }
    },
    methods: {
        getPathImg(url) {
            return new URL(url, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section id="shop">
        <div class="container flex">
            <div v-for="(item, index) in shopData" :key="index" class="col">
                <a href="">
                    <img :src="getPathImg(`../assets/img/buy-comics${item.imgName}${item.imgType}`)" alt="">
                    <p>{{ item.name }}</p>
                </a>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

#shop {
    background-color: $primary-color;
    padding: 3rem 0rem;

    .container {

        column-gap: 1rem;

        .col {
            width: calc(100% / 5 - 1rem);

            a {
                display: flex;
                justify-content: center;
                align-items: center;

                p {
                    margin-left: 1rem;
                    margin-right: 2.5rem;
                    font-size: 0.9rem;
                }

                img {
                    height: 60px;
                }
            }
        }
    }
}
</style>