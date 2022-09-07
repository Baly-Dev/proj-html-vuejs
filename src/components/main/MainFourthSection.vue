<template>
<section id="fourthSection">
    <div class="container-large">
        <div class="row">
            <div class="col-12 d-flex flex-content-center">
                <h2 class="text-primary-dark">Recent Courses</h2>
            </div>
            <div class="col-12 d-flex flex-content-center">
                <div class="categories">
                    <div v-for="(category, i) in categories" :key="i" :class="'category text-normal ' + category.class">{{category.name}}</div>
                </div>
            </div>
        </div>

        <div v-if="!showAll" class="row card-group">
            <CourseCard v-for="(course, i) in courses.slice(0, 12)" :key="i"
            :course="course"
            />
        </div>
        <div v-else class="row card-group">
            <CourseCard v-for="(course, i) in courses" :key="i"
            :course="course"
            />
        </div>

        <div class="row flex-content-center">
            <a v-if="!showAll" @click.prevent="showAll = !showAll" class="btn btn-red" href="">Show All</a>
            <a v-else @click.prevent="showAll = !showAll" class="btn btn-red" href="">Show Less</a>
        </div>
    </div>
</section>
</template>

<script>
import CourseCard from '../child_components/CourseCard.vue';
export default {
    name: 'MainFourthSection',
    data(){
        return{
            showAll: false
        }
    },
    props:{
        courses: Array,
        categories: Array
    },
    components:{
        CourseCard
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

section{
    padding: 120px 0px;

    .row:nth-child(1),
    .row:nth-child(2){
        margin-bottom: 60px;
    }

    .categories{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 45px;
        margin-top: 35px;
        align-items: center;

        .category{
            cursor: pointer;

            &:hover{
                color: $text-dark;
            }
        }
        .active{
            background-color: $secondary-gray;
            padding: 15px 20px;
            border-radius: 35px;
        }
    }
}
</style>