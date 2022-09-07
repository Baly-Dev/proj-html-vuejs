<template>
<section id="heighthSection">
    <div class="container">
        <div class="row">
            <div class="col-6">
                <div class="testimonial">
                    <h3 class="text-primary-dark">Investing for Your Future</h3>
                    <p class="text-normal content">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi distinctio ducimus quasi sapiente eaque. Quod, deserunt? In inventore soluta voluptate a sequi ea officiis reprehenderit, impedit nesciunt, consequatur nostrum eaque sit aut. Exercitationem accusamus laborum tempore quae quis ipsum consequuntur?</p>
                    <p class="author text-primary-dark">Linda Green</p>
                    <p class="position text-light">Product Manger, Apple Inc.</p>
                </div>
                <div class="triangol"></div>
            </div>
        </div>
    </div>
</section>
</template>

<script>
export default {
    name: 'MainHeighthSection'
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

section{
    background-image: url(@/assets/img/testimonial-1-1917x640-1-1914x639.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    padding: 100px 0px;

    .col-6{
        position: relative;
        margin-left: 150px;
    }

    .testimonial{
        padding: 80px;
        background-color: #fff;

        h3{
            margin-bottom: 25px;
            font-size: 1.8em;
        }

        .content{
            margin-bottom: 25px;
            font-size: 1.2em;
            line-height: 1.2em;
        }

        .author{
            margin-bottom: 5px;
        }

        .position{
            font-size: 0.8em;
        }
    }
    .triangol{
            position: absolute;
            bottom: 45%;
            right: -30px;
            z-index: 999;
            width: 0; 
            height: 0; 
            border-top: 30px solid transparent;
            border-bottom: 30px solid transparent;
            border-left: 30px solid #fff;
        }
}
</style>