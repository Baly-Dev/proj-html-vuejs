<template>
<!-- header first section -->
<div class="first d-flex flex-align-center">
    <div class="row container-large">
        <div class="col-1 h-100">
            <div class="drop-down relative"> 
                <div @click="showLanguages = !showLanguages" class="drop-down-btn d-flex flex-align-center text-light">
                    <span>Englis</span>
                    <i class="fa-solid fa-caret-down"></i>                    
                </div>
                <ul v-show="showLanguages" class="drop-down-items d-flex flex-col absolute">
                    <li class="drop-down-item"><a class="drop-down-link" href="#">Italian</a></li>
                    <li class="drop-down-item"><a class="drop-down-link" href="#">English</a></li>
                    <li class="drop-down-item"><a class="drop-down-link" href="#">Spanish</a></li>
                </ul>
            </div>
        </div>
        <div class="col-9 h-100">
            <ul class="navigation-menu d-flex flex-lg-content-end flex-content-center ">
                <li lass="nav-item" v-for="(link, i) in navigationLinks" :key="i">
                    <a class="nav-link text-light" :href="link.url">{{ link.name }}</a>
                </li>
            </ul>
        </div>
        <div class="col-2 h-100">
            <ul class="social-menu d-flex flex-content-end ">
                <li class="nav-item" v-for="(social, i) in socialLikns" :key="i">
                    <a class="nav-link" :href="social.url">
                        <i :class="'text-light fa-brands fa-' + social.class"></i>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</div>
</template>

<script>
    export default {
        name: 'HeaderFirst',
        data(){
            return{
                showLanguages: false,
            }
        },
        props:{
            navigationLinks: Array,
            socialLikns: Array,
        },
        methods:{

        }
    }
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

.first{
    height: 40px;
    border-bottom: 1px solid $secondary-gray;

    .navigation-menu{
        gap: 25px;

        .nav-link{
            font-size: 0.8em;
            cursor: pointer;

            &:hover{
                color: $hover-primary
            }
        }
    }

    .social-menu{
        gap: 15px;

        .nav-link i{
            font-size: 0.8em;
            cursor: pointer;

            &:hover{
                color: $hover-primary
            }
        }
    }

    .drop-down-items{
        top: 25px;
    }
}
</style>