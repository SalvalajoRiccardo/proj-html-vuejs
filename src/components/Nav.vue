<template>
        <div>
            <ul id="nav" class="d-flex align-items-end">
                <li class="start" v-for="(link, index) in info" :key="index">
                    <span v-if="link.new">{{link.new}}</span>
                    <h5><a href="#">{{link.text}}</a></h5>
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
        .start{
            position: relative;
            height: 50px;
            margin-top: 45px;
            &:hover h5 a {
                color: #f2b71d;
            }
            span {
                position: absolute;
                right: -5px;
                top: -10px;
                background-color: #dc1245;
                color: white;
                font-size: 10px;
                border-radius: 2px;
            }
        }
        .start:hover .dropdown{
            display: block;
        }
        .dropdown{
            display: none;
            position: absolute;
            top: 45px;
            left: -20px;
            width: 200px;
            line-height: 40px;
            background-color: #fff;
            border-top: 3px solid #f3bf33;
            & li:hover a{
                color:#f2b71d ;
            }
            
        }

        h5 {
            margin: 0px 10px 0;
            font-weight: bold;
            
        }
    }
    
</style>