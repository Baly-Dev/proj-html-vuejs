<template>
<section id="#seventhSection">
    <div class="container-large">
        <div class="row flex-content-between">
            <div class="card d-flex flex-align-center">
                <div>
                    <img src="@/assets/img/image_box_1-221x231.png" alt="">
                </div>
                <div>
                    <h3 class="text-primary-dark">Become an Instructor</h3>
                    <p class="text-light">Teach what you love. Maserstudy gives you the tools to create a course.</p>
                    <a class="btn btn-red" href="">Start Teaching</a>
                </div>
            </div>
            <div class="card d-flex flex-align-center">
                <div>
                    <img src="@/assets/img/image_box_2-234x231.png" alt="">
                </div>
                <div>
                    <h3 class="text-primary-dark">Access for Business</h3>
                    <p class="text-light">Get unlimited access to 2,500 of top courses for your team</p>
                    <a class="btn btn-red" href="">Doing Business</a>
                </div>
            </div>
        </div>
    </div>
</section>
</template>

<script>
export default {
    name: 'MainSeventhSection'
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

section{
    padding: 80px 0px;

    .card{
        width: calc((100% / 2) - 20px);
        border: 1px solid $secondary-gray;
        padding: 50px 40px;
        gap: 35px;

        h3{
            margin-bottom: 15px;
            font-size: 2em;
        }

        p{
            margin-bottom: 30px;
            font-size: 1.2em;
            line-height: 1.2em;
        }
    }
}
</style>