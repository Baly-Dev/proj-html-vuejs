<template>
<!-- header third section -->
<div class="third">
    <div class="row container-large flex-align-center  flex-content-center h-100">
        <div class="categories-box d-flex flex-align-center flex-content-center">
            <div v-for="(category, i) in categories" :key="i" class="icon-btn">
                <i :class="'text-white fa-solid fa-' + category.class"></i>
                <a class="text-white empty-btn" href="#">{{ category.name }}</a>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'HeaderThird',
    props:{
        categories: Array
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

.third{
    background-color: $primary-blue;
    height: 60px;

    .categories-box{
        gap: 40px;
    }
}
</style>