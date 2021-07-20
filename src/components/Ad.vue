<template>
     <div id="box">
        <img class="jaf" :src="require('@/assets/img/base.jpg')" alt="base">
        <div class="text">
            <h2>Get My Exclusive Investing Book Just For $ 19.50</h2>
            <span>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et, reiciendis quae recusandae praesentium neque possimus</span>
            <a href="#"><img :src="require('@/assets/img/amaz.png')" alt="Amaz"></a>
        </div>
        <div>
            <img class="book" :src="require('@/assets/img/book.png')" alt="book">
        </div>
    </div>
</template>

<script>
export default {
name:'Ad'
}
</script>

<style lang="scss" scoped>
    #box{
        width: 100%;
        position: relative;
        .jaf{
            width: 100%;
        }
        .text{
            width: 30%;
            position: absolute;
            top: 50%;
            left: 30%;
            transform: translate(-50%, -50%);
            text-align: center;
            h2{
                font-size: 40px;
                color: #f2b91e;
                font-weight: 600;
                margin-bottom: 50px;
            }
            span{
                display: block;
                color: white;
                font-size: 30px;
                line-height: 40px;
                font-style: italic;
                margin-bottom: 50px;
            }
        }
        .book{
            position: absolute;
            bottom: 0%;
            right: 20%;
        }
    }
</style>