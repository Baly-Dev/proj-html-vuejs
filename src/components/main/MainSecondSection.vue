<template>
    <section id="secondSection">
        <div class="container-large">
            <div class="row">
                <div class="col-12">
                    <h3>Popular Development Courses</h3>
                </div>
            </div>
            <div class="row card-group">
                <CourseCard v-for="(course, i) in developmentCourses"
                :key="i"
                :course="course"
                />
            </div>
        </div>
    </section>
</template>

<script>
import CourseCard from '../child_components/CourseCard.vue';
export default {
    name: "MainSecondSection",
    props:{
        developmentCourses: Array
    },
    components: { 
        CourseCard 
    }
}
</script>

<style lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';


section{
    padding: 80px 0px;

    .row:nth-child(1){
        margin-bottom: 30px;
    }

    .card-group{
        gap: 20px;
        .card{
            width: calc((100% / 6) - 20px);
        }
        
    }
}

</style>