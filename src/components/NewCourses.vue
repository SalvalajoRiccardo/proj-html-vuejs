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
        }

        h2{
            font-family: 'Roboto Slab', serif;
            font-size: 50px;
            padding-top: 50px;
            margin-bottom: 50px;
        }
        .box-news {
            width: 60%;
            margin: 0 auto;
            .card-new{
                position: relative;
                padding: 10px;
                width: calc(100% / 3);
                img {
                    width: 100%;
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
                .price{
                    display: none;
                    position: absolute;
                    top: 25%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    font-weight: 700;
                }
                .info{
                    padding:50px 20px 20px;
                    background-color: #fff;
                    border: 1px solid lightgray;
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