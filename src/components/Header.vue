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
            <i class="fab fa-linkedin"></i>
            <i class="fab fa-instagram"></i>
            <i class="fab fa-facebook"></i>
            <i class="fab fa-twitter"></i>
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
    height: 150px;
    // #social-top{

    // }
}

</style>