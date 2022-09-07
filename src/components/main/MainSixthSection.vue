<template>
<section id="sixthSection">
    <div class="container-large">
        <div class="row">
            <div class="col-12">
                <h2 class="text-primary-dark">Popular Development Courses</h2>
                <p class="text-light">Discover our most popular corses for self learning</p>
            </div>
        </div>
        <div class="row card-group">
            <CourseCard v-for="(course, i) in courses.slice(sliderNextFirst, sliderNextSecond)"
            :key="i"
            :course="course"
            />
        </div>
        <div class="row">
            <div class="col-12 d-flex flex-content-center">
                <button @click="cardCarouselPrev()" class="prev">
                    <i class="fa-solid fa-chevron-left"></i>
                </button>
                <button @click="cardCarouselNext()" class="next">
                    <i class="fa-solid fa-chevron-right"></i>
                </button>
            </div>
        </div>
    </div>
</section>
</template>

<script>
import CourseCard from '../child_components/CourseCard.vue'
export default {
name: 'MainSixthSection',
data(){
    return{
        sliderNextFirst: 0,
        sliderNextSecond: 6
    }
},
props:{
    courses: Array
},
methods:{
    cardCarouselNext(){
        if (this.sliderNextFirst < this.courses.length - 6){
            this.sliderNextFirst++
        }
        if (this.sliderNextSecond < this.courses.length){
            this.sliderNextSecond++
        }
        return
    },
    cardCarouselPrev(){
        if (this.sliderNextFirst > 0){
            this.sliderNextFirst--
        }
        if (this.sliderNextSecond > 6){
            this.sliderNextSecond--
        }
    }
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
    background-color: $primary-gray;
    padding: 80px 0px;
    .row:nth-child(1){
        h2,
        p{
            text-align: center;
        }

        h2{
            margin-bottom: 20px;
        }
    }

    .row:nth-child(2){
        margin-bottom: 30px;
    }

    .row:nth-child(3){
        button{
            cursor: pointer;
            padding: 10px;
            border: 1px solid $tertiary-gray;
            color: $tertiary-gray;
            background-color: $primary-gray;

            &:hover{
                background-color: $secondary-blue;
                border-color: $secondary-blue;
            }
        }
    }
}
</style>