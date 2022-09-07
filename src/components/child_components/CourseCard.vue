<template>
    <div class="card">
        <div class="card-header">
            <img :src="require('@/assets/img/' + course.cover)" alt="">
        </div>
        <div class="card-body">
            <a class="content-category text-light" href="">{{ course.category }} ></a>
            <p class="text-primary-dark">{{ course.title }}</p>
            <hr class="divider">
        </div>
        <div class="card-footer d-flex flex-content-between">
            <div class="ranking">
                <img v-for="n in course.rank" :key="n" src="@/assets/img/starfull.svg" alt="">
                <img v-for="n in 5 - course.rank" :key="n + course.rank" src="@/assets/img/staremptyl.svg" alt="">
            </div>
            <div class="prices">
                <div class="d-flex flex-col" v-if="course.sale > 0">
                    <small class="discount text-light">${{course.price}}</small>
                    <small class="price">${{course.actualPrice}}</small>
                </div>
                <div v-else>
                    <small class="discount text-light">${{course.price}}</small>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'CourseCard',
    props:{
        course: Object
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

.card{
    border: 1px solid $secondary-gray;
    height: 355px;
    
    .card-header{
        img{
            width: 100%;
            object-fit: cover;
            object-position: center;
        }
    }

    .card-body{
        padding: 0px 10px;
        padding-top: 10px;

        a{
            font-size: 0.8em;
        }

        p{
            font-size: 0.9em;
            margin-top: 15px;
            line-height: 1.3em;
        }

        .divider{
            border: 1px solid $secondary-gray;
            margin: 20px 0px;
        }
    }

    .card-footer{
        padding: 0px 10px;

        .prices{
            small{
                font-size: 0.8em;
                text-align: right;
            }

            small:nth-child(1){
                margin-bottom: 5px;
                text-decoration: line-through;
            }
        }
    }
}
</style>