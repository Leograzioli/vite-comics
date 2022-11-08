<script>
export default {
    name: 'AppShop',
    data() {
        return {

        }
    }
}
</script>

<template>
    <section id="shop">
        <div class="container flex">
            <div class="col">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                <p>DIGITAL COMICS</p>
            </div>
            <div class="col">
                <img src="../assets/img/buy-comics-merchandise.png" alt="">
                <p>DC MERCHANDISE</p>
            </div>
            <div class="col">
                <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                <p>SUBSCRIPTION</p>
            </div>
            <div class="col">
                <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                <p>COMIC SHOP LOCATOR</p>
            </div>
            <div class="col">
                <img class="visa" src="../assets/img/buy-dc-power-visa.svg" alt="">
                <p>DC POWER VISA</p>
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

        .col {
            width: calc(100% / 5);

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

            .visa {
                height: 40px;
            }
        }
    }

}
</style>