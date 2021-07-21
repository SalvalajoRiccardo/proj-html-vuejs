<template>
    <div id="foot">
        <div class="f-box d-flex">
            <div class="box">
                <h4>About</h4>
                <span> <a href="#">Masterstudy</a>  is Education WordPress theme featured by Learning Management System (LMS) for online education.</span>
                <span>Developed by <a href="#">StylemixThemes</a>. </span>
                
            </div>

            <div class="box">
                <h4>Contact</h4>
                <span>USA, Callifornia 20, First Avenue, Callifornia</span>
                <br>
                <span>Tel.: +1 212 458 300 32</span>
                <span>Fax: +1 212 375 24 14</span>
                <a href="#">info@masterstudy.com</a>
            </div >

            <div class="box">
                <h4>Pages</h4>
                <ul class="d-flex justify-content-between">
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Shortcodes</a></li>
                    <li><a href="#">Courses</a></li>
                    <li><a href="#">Membership A...</a></li>
                    <li><a href="#">Typography</a></li>
                </ul>
            </div>

            <div class="box">
                <h4>Blog</h4>
                <div class="jab d-flex align-items-center">
                    <div>
                        <img :src="require('@/assets/img/august.jpeg')" alt="august">

                    </div>
                    <div>
                        <span>Our main target is to “Developing Yourself as a Leader”</span>
                        <a href="#"> August 9, 2018</a>
                    </div>
                </div>

                <div class="jab d-flex align-items-center">
                    <div>
                        <img :src="require('@/assets/img/june.jpeg')" alt="june">

                    </div>
                    <div>
                        <span>Those Other College Expenses You Aren`t Thinking About</span>
                        <a href="#">June 3, 2015</a>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    name:'Footer'
}
</script>

<style lang="scss" scoped>
    #foot{
        position: fixed;
        z-index: -5000;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 300px;
        background-color: #f2b91e;
        color: black;
        padding: 50px 0 0px;
        .f-box{
            width: 70%;
            margin: 0 auto;
            .box{
                width: 25%;
                margin: 0 20px 10px;
                .jab{
                    line-height: 16px;
                    margin-bottom: 20px;
                    img{
                        width: 70px;
                        margin-right: 10px;
                    }
                    span{
                        font-family: 'Roboto Slab', serif;
                        font-weight: 500;
                        font-size: 16px;
                    }
                    &:hover span{
                        color: white;

                    }
                }
                h4{
                    font-family: 'Roboto Slab', serif;
                    font-weight: 600;
                    font-size: 30px;
                }
                span{
                    display: block;
                }
                ul{
                    list-style-type: disc;
                    flex-wrap: wrap;
                    li{
                        width: 45%;
                        margin: 10px 0;
                        &:hover {
                            color: white;
                            a{
                                color: white;
                            }
                        }
                    }
                }
            }
        }
    }
</style>