<template>
    <main>
        <MainFirstSection />
        <MainSecondSection 
        :developmentCourses="developmentCourses"
        />        
    </main>
</template>

<script>
import MainFirstSection from './MainFirstSection.vue'
import MainSecondSection from './MainSecondSection.vue';
export default {
    name: 'TheMain',
    props:{
        developmentCourses: Array
    },
    components:{
        MainFirstSection,
        MainSecondSection
    }
}
</script>

<style>

</style>
