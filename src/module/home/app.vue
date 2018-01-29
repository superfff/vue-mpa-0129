<template>
    <div>
        <img src="./images/logo.png">
        <img src="./images/123.jpg" alt="">
    </div>
</template>

<script>

export default {
    data(){
        return {

        }
    },
    created(){

    },
    methods: {

    }
}
</script>

<style scoped>
    div{
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    img{
        margin-bottom: 10px;
        object-fit: contain;
    }
</style>
