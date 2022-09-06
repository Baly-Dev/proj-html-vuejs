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
                    <div class="input-box">
                        <input class="search-bar" type="text" name="search" id="headerSearchBar" placeholder="Search courses">
                        <button class="search-btn" type="button"><i class="fa-solid fa-magnifying-glass"></i></button>
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
    export default {
        name: 'HeaderSecond',
        data(){
            return{
                showCategories: false
            }
        },
        props:{
            categories: Array,
        }
    }
</script>

<style scoped lang="scss">
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

    .input-box{
        margin-right: 30px;
        .search-bar,
        .search-btn{
            height: 40px;
            padding: 0 15px;
        }

        .search-bar{
            width: 450px;
            border: 1px solid $secondary-gray;
            background-color: $secondary-gray;
            color: $text-light;

            &::placeholder{
                color: $text-light;
            }

            &:active,
            &:focus{
                outline: none;
            }
        }

        .search-btn{
            border: 1px solid $secondary-blue;
            background-color: $secondary-blue;
            color: #fff;
            cursor: pointer;

            &:hover{
                border: 1px solid $primary-blue;
                background-color: $primary-blue;
            }
        }
    }
}
</style>
