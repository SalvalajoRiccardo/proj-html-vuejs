<template>
        <div>
            <ul id="nav" class="d-flex align-items-end">
                <li class="start" v-for="(link, index) in info" :key="index">
                    <span v-if="link.new">{{link.new}}</span>
                    <h5><a href="#">{{link.text}}</a></h5>
                    <ul class="dropdown" v-if="link.drops" >
                        <li :class="(downlink.styles) ? 'start-right' : ''" v-for="(downlink, index) in link.drops" :key="'A'+ index">
                            <a href="#">
                                {{downlink.link}}
                                <i v-if="downlink.styles" class="fas fa-chevron-right"></i> 
                            </a>
                            <ul v-if="downlink.styles">
                                <li v-for="(last,index) in downlink.styles " :key="'B'+ index">
                                    <a href="#">{{last.ext}}</a>
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
                border-radius: 3px 3px 3px 0;
                padding: 0 3px;
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
            &::after {
                content: '';
                position: absolute;
                top:-10px;
                left: 50%;
                margin-left: -50px;
                width: 0;
                height: 0;
                border-bottom: solid 10px #f3bf33;
                border-left: solid 10px transparent;
                border-right: solid 10px transparent;
                }
            & li:hover > a{
                color:#f2b71d ;
            }
            i {
                margin-left: 40px ;
            }
            .start-right{
                position: relative;
               ul {
                    
                    display: none;
                    position: absolute;
                    left: 100%;
                    top: -50px;
                    li {
                        width: 100px;
                    }
               }
                &:hover ul{
                display: block;
                background-color: #fff;
            }
        }
        }

        h5 {
            margin: 0px 10px 0;
            font-weight:600;
            
        }
    }
    
</style>