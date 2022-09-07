<template>
<!-- header second section -->
<div class="second">
    <div class="row container-large flex-align-center h-100">
        <div class="col-2">
            <img class="brand" src="@/assets/MasterStudy.svg" alt="Logo">
        </div>
        <div class="col-8">
            <div class="row flex-align-center">
                <div class="col-2">
                    <div class="drop-down relative">
                        <div @click="showCategories = !showCategories" class="drop-down-btn d-flex flex-align-center text-light">
                            <i class="fa-solid fa-bars"></i>
                            <span>Categories</span>              
                        </div>
                        <ul v-show="showCategories" class="drop-down-items d-flex flex-col absolute">
                            <li v-for="(category, i) in categories" :key="i" class="drop-down-item">
                                <a class="drop-down-link" href="#">{{ category.name }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-10 d-flex flex-row flex-align-center">
                    <div class="w-60">
                        <InputField 
                        :inputInfo="inputInfo"
                        />
                    </div>
                    <div class="btn-box">
                        <div class="icon-btn">
                            <i class="text-light fa-solid fa-bullhorn"></i>
                            <a class="text-light empty-btn" href="#">Become an Instructor</a>
                        </div>
                        <div class="icon-btn">
                            <i class="text-light fa-solid fa-briefcase"></i>
                            <a class="text-light empty-btn" href="#">For Enterprise</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-2 d-flex flex-row flex-content-end flex-align-center">
            <div class="btn-box">
                <div class="icon-btn">
                    <i class="text-light fa-solid fa-user"></i>
                    <a class="text-light empty-btn" href="#">Log in</a>
                </div>
                <a class="btn btn-red" href="">Sign Up</a>
                <div class="icon-btn">
                    <i class="text-light fa-regular fa-bookmark"></i>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import InputField from '../child_components/InputField.vue';
export default {
    name: 'HeaderSecond',
    data(){
        return{
            showCategories: false,
            inputInfo:{   
                type: 'text', 
                placeholder: 'Search Courses',
                id: 'searchBar',
                icon: 'magnifying-glass',
                btnText: ''
            } 
        }
    },
    props:{
        categories: Array,
    },
    components:{
        InputField
    }
}
</script>

<style lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

.second{
    height: 80px;

    .drop-down-btn span{
        text-transform: uppercase;
    }

    .drop-down-items{
        top:  25px;
    }
}
</style>
