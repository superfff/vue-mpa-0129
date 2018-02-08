<template>
    <div>
        <img src="./images/logo.png">
        <img src="./images/123.jpg" alt="">
        <p>static1</p>
        <img src="~static/123.jpg" alt="">
        <p>background-image</p>
        <div class="img"></div>
        <hello></hello>
        <p>{{info}}</p>
    </div>
</template>

<script>
// 引入公共文件
import Libs from 'assets/lib';
import hello from 'components/HelloWorld';
import ss from 'static/test.js';

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

        ss();
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

    .img{
        width: 555px;
        height: 300px;
        background-image: url('.images/123.jpg');
        background-repeat: no-repeat;
        background-size: 100%;
        margin: 0 auto;
    }
</style>
