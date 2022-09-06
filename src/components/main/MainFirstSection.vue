<template>
    <section id="firstSection">
        <div class="container">
            <div class="row">
                <div class="col-5 left">
                    <h1 class="text-white">Udemy Affiliate Sales</h1>
                    <p class="text-white">Monetize yout audience and attract new customers with Udemy!</p>
                </div>
                <div class="col-7 right">
                    <div class="diagonal"></div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "MainFirstSection"
    }
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

section{
    background-color: $primary-red;
    background-image: url(@/assets/img/slide-1.jpg);

    background-repeat: no-repeat;
    background-position: right;
    background-size: contain;

    .left{
        display: flex;
        flex-direction: column;
        justify-content: center;
        height: 400px;
        background-color: $primary-red;
        
        p{
            font-size: 1.2em;
            margin-top: 10px;
            line-height: 1.3em;
        }
    }

    .right{
        .diagonal{
            left: 0;
            width: 0;
            height: 0;
            border-bottom: 400px solid $primary-red;
            border-right: 220px solid transparent;
        }
    }
}
</style>