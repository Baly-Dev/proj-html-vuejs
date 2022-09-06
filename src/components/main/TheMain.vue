<template>
    <main>
        <MainFirstSection />
        <MainSecondSection 
        :developmentCourses="developmentCourses"
        />
        <MainThirdSection />      
    </main>
</template>

<script>
import MainFirstSection from './MainFirstSection.vue'
import MainSecondSection from './MainSecondSection.vue';
import MainThirdSection from './MainThirdSection.vue';
export default {
    name: 'TheMain',
    props:{
        developmentCourses: Array
    },
    components:{
        MainFirstSection,
        MainSecondSection,
        MainThirdSection
    }
}
</script>

<style>

</style>
