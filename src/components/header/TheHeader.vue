<template>
    <header>
        <nav class="navbar">
            <HeaderFirst 
            :navigationLinks="navigationLinks" 
            :socialLikns="socialLikns"
            />

            <HeaderSecond 
            :categories="categories"
            />

            <HeaderThird 
            :categories="categories"
            />

        </nav>
    </header>
</template>

<script>
import HeaderFirst from './HeaderFirst.vue'
import HeaderSecond from './HeaderSecond.vue'
import HeaderThird from './HeaderThird.vue'
export default {
    name: 'TheHeader',
    props:{
        categories: Array,
        socialLikns: Array
    },
    data(){
        return{
            navigationLinks:[
                {name: 'Home', url: '#'},
                {name: 'Pages', url: '#'},
                {name: 'Course Formats', url: '#'},
                {name: 'Courses', url: '#'},
                {name: 'Demos', url: '#'}
            ]
        }
    },
    components:{
        HeaderFirst,
        HeaderSecond,
        HeaderThird
}
}
</script>

<style lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

header{
    /* globals */
    .drop-down-btn{
        font-size: 0.8em;
        gap: 8px;
        cursor: pointer;

        &:hover{
            color: $hover-primary
        }
    }

    .drop-down-items{
        min-width: 100px;
        padding: 15px;
        gap: 15px;
        border: 1px solid $secondary-gray;
        background-color:#fff;
        border-radius: 6px;
        font-size: 0.8em;

        .drop-down-link{
            color: $text-dark;
            &:hover{
                color: $hover-primary
            }
        }
    }

    .btn-box{
        margin-left: auto;
        display: flex;
        align-items: center;
        gap: 20px;
        
    }

    .icon-btn{
        cursor: pointer;

        &:hover i,
        &:hover .empty-btn{
            color: $hover-primary;
        }

        & i{
            font-size: 0.8em;
            margin-right: 10px;
        }
        & .empty-btn{
            font-size: 0.9em;
        }
    }
}
</style>