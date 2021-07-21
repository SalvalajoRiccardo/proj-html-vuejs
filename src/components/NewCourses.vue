<template>
    <section>
        <div>
            <div>
                <h2>New Courses</h2>
            </div>
            <!-- special section -->
            <div class="box-news d-flex">
                <div class="card-new">
                    <img :src="require('@/assets/img/dj.jpeg')" alt="dj">
                    <h3 class="price">$59</h3>
                    <span class="special">special</span>
                    <div class="info">
                        <h5>How to be a DJ? Make Electronic Music</h5> 
                        <span class="grey">Electronic</span>
                        <hr>
                        <div class="d-flex justify-content-between">
                            <div>
                                <i class="fas fa-signal"></i>
                                <span> Advanced </span>
                            </div>
                            <div>
                                <i class="fas fa-bars"></i>
                                <span> 8 Lectures </span>
                            </div>
                            <div>
                                <i class="far fa-clock"></i>
                                <span> 6 hours </span>
                            </div>
                            
                        </div>
                    </div>
                </div>
                
                <div class="card-new">
                    <img :src="require('@/assets/img/unreal.png')" alt="unreal">
                    <h3 class="price">$78</h3>
                    <span class="special">special</span>
                    <div class="info">
                        <h5>Nvidia and UE4 Technologies Practice</h5> 
                        <span class="grey">Nvidia</span>
                        <hr>
                        <div class="d-flex justify-content-between">
                            <div>
                                <i class="fas fa-signal"></i>
                                <span> Advanced </span>
                            </div>
                            <div>
                                <i class="fas fa-bars"></i>
                                <span> 8 Lectures </span>
                            </div>
                            <div>
                                <i class="far fa-clock"></i>
                                <span> 6 hours </span>
                            </div>
                            
                        </div>
                    </div>
                </div>

                <div class="card-new">
                    <img :src="require('@/assets/img/photo.jpeg')" alt="photo">
                    <h3 class="price">$50</h3>
                    <span class="special">special</span>
                    <div class="info">
                        <h5>Fashion Photography from professional</h5> 
                        <span class="grey">Fashion</span>
                        <hr>
                        <div class="d-flex justify-content-between">
                            <div>
                                <i class="fas fa-signal"></i>
                                <span> Advanced </span>
                            </div>
                            <div>
                                <i class="fas fa-bars"></i>
                                <span> 6 Lectures </span>
                            </div>
                            <div>
                                <i class="far fa-clock"></i>
                                <span> 6 hours </span>
                            </div>
                            
                        </div>
                    </div>
                </div>
            </div>
            <!-- special section -->

            <!-- normal section -->
            <div class="box-news d-flex">
                <div class="card-new">
                    <img :src="require('@/assets/img/fashion.jpeg')" alt="fashion">
                    <h3 class="price">$90</h3>
                    <div class="info">
                        <h5>Design Instruments for Communication</h5> 
                        <span class="grey">Communication</span>
                        <hr>
                        <div class="d-flex justify-content-between">
                            <div>
                                <i class="fas fa-signal"></i>
                                <span> Intermediate </span>
                            </div>
                            <div>
                                <i class="fas fa-bars"></i>
                                <span> 6 Lectures </span>
                            </div>
                            <div>
                                <i class="far fa-clock"></i>
                                <span> 6 hours </span>
                            </div>
                            
                        </div>
                    </div>
                </div>

                <div class="card-new">
                    <img :src="require('@/assets/img/des.jpg')" alt="des">
                    <h3 class="price">$70</h3>
                    <div class="info">
                        <h5>Make your Concept Right and Beautiful</h5> 
                        <span class="grey">Art</span>
                        <hr>
                        <div class="d-flex justify-content-between">
                            <div>
                                <i class="fas fa-signal"></i>
                                <span> Intermediate </span>
                            </div>
                            <div>
                                <i class="fas fa-bars"></i>
                                <span> 6 Lectures </span>
                            </div>
                            <div>
                                <i class="far fa-clock"></i>
                                <span> 6 hours </span>
                            </div>
                            
                        </div>
                    </div>
                </div>

                <div class="card-new">
                    <img :src="require('@/assets/img/byc.jpeg')" alt="byc">
                    <h3 class="price">$20</h3>
                    <div class="info">
                        <h5>Road Bike Manual or How to Be a Champion.</h5> 
                        <span class="grey">Bicycling</span>
                        <hr>
                        <div class="d-flex justify-content-between">
                            <div>
                                <i class="fas fa-signal"></i>
                                <span> Beginner </span>
                            </div>
                            <div>
                                <i class="fas fa-bars"></i>
                                <span> 6 Lectures </span>
                            </div>
                            <div>
                                <i class="far fa-clock"></i>
                                <span> 6 hours </span>
                            </div>
                            
                        </div>
                    </div>
                </div>
            </div>
            <!-- normal section -->
            <div>
                <button>load more</button>
            </div>
        </div>
    </section>
</template>

<script>
export default {
name:'NewCourses'
}
</script>

<style lang="scss" scoped>
    @import '@/style/commons.scss';
    section{
        background-color: #edf2f5;
        text-align: center;
        button{
            margin-top: 50px;
            margin-bottom: 100px;
            padding:10px 20px;
            border-radius: 30px;
            border: none;
            background-color:#f2b91e ;
            font-family: 'Roboto Slab', serif;
            font-weight: 600;
            text-transform: uppercase;
            color: white;
            transition: all .3s;
            position: relative;
            overflow: hidden;
            z-index: 1;
            // per effetto over
            &:after {
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background-color: #f2b91e;
                border-radius: 10rem;
                z-index: -2;
            }
            &:before {
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;
                width: 0%;
                height: 100%;
                background-color: darken(#f2b91e, 15%);
                transition: all .3s;
                border-radius: 10rem;
                z-index: -1;
            }
            &:hover {
                color: #fff;
                &:before {
                width: 100%;
                }
            }
        }
        
       
        h2{
            font-family: 'Roboto Slab', serif;
            font-size: 50px;
            padding-top: 50px;
            margin-bottom: 50px;
        }
        .box-news {
            width: 70%;
            margin: 0 auto;
            .card-new{
                position: relative;
                margin: 20px;
                width: calc(100% / 3);
                &:hover {
                    box-shadow: 0px 2px 10px 0px #888888;
                }
                &:hover img {
                    filter: brightness(50%);
                }
                &:hover .price {
                    display: block;
                }
                &:hover h5 {
                    color: #f2b91e;
                }
                .price{
                    display: none;
                    position: absolute;
                    z-index: 400;
                    top: 25%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    font-weight: 700;
                    color: white;
                }
                img {
                    width: 100%;
                    transition: 0.5s;

                }

                
                .special{
                    display: block;
                    position: absolute;
                    top: 5%;
                    right: 5%;
                    background-color: #f09b23;
                    color: white;
                    padding: 3px 5px;
                    border-radius: 3px;
                    text-transform: uppercase;
                    font-size: 12px;
                }
                
                .info{
                    padding:50px 20px 20px;
                    background-color: #fff;
                    border: 1px solid lightgray;
                    // height: 230px;
                    hr{
                        color: grey;
                    }
                    h5{
                        font-family: 'Roboto Slab', serif;
                        margin-bottom: 20px;
                    }
                    .grey{
                        color: lightgrey;
                        display: block;
                        margin-bottom: 20px;
                    }
                    i {
                        color: #f2b91e;
                    }
                }
            }
        }
    }
</style>