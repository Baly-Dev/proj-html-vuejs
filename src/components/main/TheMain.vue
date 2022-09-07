<template>
    <main>
        <MainFirstSection />
        <MainSecondSection 
        :developmentCourses="developmentCourses"
        />
        <MainThirdSection />   
        <MainFourthSection
        :courses="courses"
        :categories="categories"
        />
        <MainFifthSection />
        <MainSixthSection
        :courses="courses"
        />
        <MainSeventhSection />
        <MainHeighthSection />
    </main>
</template>

<script>
import MainFirstSection from './MainFirstSection.vue'
import MainSecondSection from './MainSecondSection.vue';
import MainThirdSection from './MainThirdSection.vue';
import MainFourthSection from './MainFourthSection.vue';
import MainFifthSection from './MainFifthSection.vue';
import MainSixthSection from './MainSixthSection.vue';
import MainSeventhSection from './MainSeventhSection.vue';
import MainHeighthSection from './MainHeighthSection.vue'

export default {
    name: 'TheMain',
    props:{
        developmentCourses: Array,
        courses: Array,
        categories: Array
    },
    components:{
        MainFirstSection,
        MainSecondSection,
        MainThirdSection,
        MainFourthSection,
        MainFifthSection,
        MainSixthSection,
        MainSeventhSection,
        MainHeighthSection
    }
}
</script>