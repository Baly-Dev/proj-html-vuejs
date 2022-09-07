<template>
<footer>
    <div class="first">
        <div class="container row">
            <div class="col-3">
                <div class="footer-item">
                    <h4 class="text-white">About</h4>
                    <p class="text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum molestiae, tempora omnis cumque facilis ab impedit natus iure eum! Voluptatem?</p>
                </div>
            </div>
            <div class="col-3">
                <div class="footer-item">
                    <h4 class="text-white">Content</h4>
                    <p class="text-white">USA California 20, First Avenue, California</p>
                    <p class="text-white">Tel.: +212 458 300 32</p>
                    <p class="text-white">Tel.: +212 458 300 32</p>
                    <p class="text-light">info@maserstudy.com</p>
                </div>
            </div>
            <div class="col-3">
                <div class="footer-item">
                    <h4 class="text-white">Social</h4>
                    <div class="social-items">
                        <li v-for="(social, i) in socialLikns" :key="i" :class="'social-item ' + social.color">
                            <a class="text-white" :href="social.url">
                                <i :class="'text-white fa-brands fa-' + social.class"></i>
                            </a>
                        </li>
                    </div>
                </div>
            </div>
            <div class="col-3">
                <div class="footer-item">
                    <img src="@/assets/img/Top-udemy-courses-90-percent-off.jpg" alt="">
                </div>
            </div>
        </div>
    </div>
    <div class="second">
        <div class="container row h-100">
            <div class="d-flex flex-align-center">
                <img src="@/assets/img/footer-logo2x-50x56.png" alt="">
                <small class="text-white">Copyright © 2022. Lorem ipsum dolor sit amet.</small>
            </div>
        </div>
    </div>
</footer>
</template>

<script>
export default {
    name: 'TheFooter',
    props:{
        socialLikns: Array
    }
}
</script>

<style lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

footer{
background-color: $primary-blue;

.first{
    border-bottom: 1px solid $secondary-gray;
    padding: 30px 0px;

    .footer-item{
        padding: 15px;

        h4{
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        p{
            margin-bottom: 10px;
            font-size: 0.9em;
            line-height: 1.2em;
        }

        img{
            width: 100%;
            object-fit: cover;
        }
    }

    .fb{
        background-color: #3C5998;
        color: #fff;
    }

    .ig{
        background-color: #C12BA3;
        color: #fff;
    }

    .in{
        background-color: #0277B5;
        color: #fff;
    }

    .tw{
        background-color: #1EA1F1;
        color: #fff;
    }

    .gp{
        background-color: #DB4637;
        color: #fff;
    }

    .yt{
        background-color: #BD0B1C;
        color: #fff;
    }

    .social-items{
        display: flex;
        flex-wrap: wrap;

        .social-item{
            width: 50px;
            height: 50px;

            display: flex;
            justify-content: center;
            align-items: center;

            margin-right: 10px;
            margin-bottom: 10px;
            border-radius: 50%;
            i{
                font-size: 1.8em;
            }
        }
    }
}

.second{
    padding: 15px 0px;
    img{
        margin-right: 15px;
        width: 30px;
    }
}

}
</style>