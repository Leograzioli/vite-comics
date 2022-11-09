<script>
export default {
    name: 'AppShop',
    data() {
        return {
            shopData: [
                {
                    name: 'DIGITAL COMICS',
                    imgName: '-digital-comics.png',
                },
                {
                    name: 'DC MERCHANDISE',
                    imgName: '-merchandise.png',
                },
                {
                    name: 'SUBSCRIPTION',
                    imgName: '-subscriptions.png',
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    imgName: '-shop-locator.png',
                },
                {
                    name: 'DC POWER VISA',
                    imgName: '-power-visa.svg',
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
                    <img :src="getPathImg(`../assets/img/buy-comics${item.imgName}`)" :alt="item.name">
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
            width: calc(100% / 5);

            a {
                display: flex;
                justify-content: center;
                align-items: center;

                p {
                    margin-left: 1rem;
                    margin-right: 2.5rem;
                    font-size: 0.9rem;
                    color: white;
                }

                img {
                    height: 60px;
                }
            }
        }
    }
}
</style>