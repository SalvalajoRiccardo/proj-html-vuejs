<template>
    <div id="head" class="d-flex justify-content-center align-items-center">
        <!-- logo -->
        <div id="logo">
            <img :src="require('../assets/img/MasterStudy-1.svg')" alt="MasterStudy">
        </div>
        <!-- navbar -->
        <Nav :info="apiT"/>

        <!-- social -->
        <div id="social-top">
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
        </div>

    </div>
  
</template>

<script>
import Nav from '../components/Nav.vue'
export default {
    name: 'Header',
    props: ['api'],
    components: {
        Nav
    },
    data(){
        return{
            apiT : this.api
        }
    }
    
}
</script>

<style lang="scss" scoped>
#head{
    width: 100%;
    height: 150px;
    background-color: #fff;
    #logo{
        
        img {
            margin-right: 200px;
        }
    }
    #social-top{
        font-size: 20px;
        margin-left: 50px;
        a {
            margin: 0 10px;
        }
        a:hover{
            color: #f2b71d;
        }
    }
}

</style>