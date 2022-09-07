<template>
<section id="fifthSection">
    <div class="row container">
        <div class="col-6 left">
            <h3 class="text-white">Subscribe our Newsletter</h3>
            <p class="text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores facilis obcaecati praesentium libero, quasi minus!</p>
        </div>
        <div class="col-6 right">
            <label class="text-white" for="newsLetter">Your E-mail Address</label>
            <InputField 
            :inputInfo="inputInfo"
            />
        </div>
    </div>
</section>
</template>

<script>
import InputField from '../child_components/InputField.vue';
export default {
    name: 'MainFifthSection',
    data(){
        return{
            inputInfo:{   
                type: 'email',
                placeholder: 'Enter your Email',
                id: 'newsLetter',
                icon: '',
                btnText: 'SUBSCRIBE'
            }
        }
    },
    components:{
        InputField
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

section{
    background-color: $primary-red;
    padding: 40px 0px;

    .left{
        h3{
            margin-bottom: 10px;
        }
    }
    
    .right{
        label{
            display: block;
            margin-bottom: 10px;
            text-transform: uppercase;
        }
    }
}

</style>