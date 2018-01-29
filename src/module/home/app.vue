<template>
    <div>
        <img src="./images/logo.png">
        <img src="./images/123.jpg" alt="">
        <hello></hello>
        <p>{{info}}</p>
    </div>
</template>

<script>
// 引入公共文件
import Libs from 'assets/lib';
import hello from 'components/HelloWorld';

export default {
    components: {
        hello
    },
    data(){
        return {
            info: ''
        }
    },
    created(){
        this.info = Libs.C.version;

        let obj = {
            a: 1,
            b: 'ab'
        };
        console.log(Libs.F.obj_str(obj));

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
    p{
        text-align: center;
    }
</style>
