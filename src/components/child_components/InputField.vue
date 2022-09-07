<template>
<div class="input-box">
    <input class="input-bar" :type="inputInfo.type" name="search" :id="inputInfo.id" :placeholder="inputInfo.placeholder">
    <button class="input-btn" type="button">{{inputInfo.btnText}}<i v-show="inputInfo.icon != ''" :class="'fa-solid fa-' + inputInfo.icon"></i></button>
</div>
</template>

<script>
export default {
    name: 'InputField',
    props:{
        inputInfo: Object
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

.input-box{
    display: flex;
    flex-wrap: nowrap;
    width: 100%;

    .input-bar,
    .input-btn{
        height: 40px;
        padding: 0 15px;
    }

    .input-bar{
        border: 1px solid $secondary-gray;
        background-color: $secondary-gray;
        width: 100%;
        color: $text-light;

        &::placeholder{
            color: $text-light;
        }

        &:active,
        &:focus{
            outline: none;
        }
    }

    .input-btn{
        border: 1px solid $secondary-blue;
        background-color: $secondary-blue;
        color: #fff;
        cursor: pointer;

        &:hover{
            border: 1px solid $primary-blue;
            background-color: $primary-blue;
        }
    }
    }
</style>