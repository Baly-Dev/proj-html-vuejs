<template>
    <section id="thirdSection">
        <div class="row container">
            <div class="col-5 left">
                <div>
                    <h2 class="text-primary-dark">Limitless learning, more Possibilities</h2>
                    <p>Online courses open the opportunity to learning to almost anyone, regardless of their scheduling commitment</p>
                </div>
                <a class="btn btn-red" href="">Read More</a>
            </div>
            <div class="col-7 right">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MainThirdSection'
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

section{
    padding: 120px 0px;

    background-image: url(@/assets/img/bg.png);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    .left{
        h2{
            margin-bottom: 15px;
            line-height: 1.2em;
        }
        p{
            line-height: 1.5em;
        }
        div{
            margin-bottom: 40px;
        }
    }
}
</style>