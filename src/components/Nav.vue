<template>
        <div>
            <ul id="nav" class="d-flex">
                <li v-for="(link, index) in info" :key="index">
                    <h3><a href="#">{{link.text}}</a></h3>
                    <ul class="dropdown" v-if="link.drops" >
                        <li v-for="(downlink, index) in link.drops" :key="'A'+ index">
                            <a href="#">
                                {{downlink.link}}
                                <i v-if="downlink.styles" class="fas fa-chevron-right"></i> 
                            </a>
                            <ul v-if="downlink.styles">
                                <li v-for="(last,index) in downlink.styles " :key="'B'+ index">
                                    {{last.ext}}
                                </li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>

        </div>
</template>

<script>
export default {
    name: 'Nav',
    props:['info']
}
</script>

<style lang="scss" scoped>
    @import '@/style/commons.scss';
    #nav {
        position: relative;
        
        .dropdown{
            position: absolute;
            
        }

    }
    
</style>