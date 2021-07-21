<template>
    <div class="num">
        <div class="num-box d-flex justify-content-between align-items-center">
            <div class="num-card d-flex align-items-center">
                <i class="fas fa-user-friends"></i>
                <div>
                    <h3>7500</h3>
                    <span>Online Learner</span>
                </div>
            </div>
            <div class="num-card d-flex align-items-center">
                <i class="fab fa-youtube"></i>
                <div>
                    <h3>55</h3>
                    <span>Video Coursesr</span>
                </div>
            </div>
            <div class="num-card d-flex align-items-center">
                <i class="fas fa-photo-video"></i>
                <div>
                    <h3>1025</h3>
                    <span>Sliders &#38; Images</span>
                </div>
            </div>
            <div class="num-card d-flex align-items-center">
                <i class="fas fa-thumbs-up"></i>
                <div>
                    <h3>3380</h3>
                    <span>Excellent Reviews</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
name: 'Numbers'
}
</script>

<style lang="scss" scoped>
    @import '@/style/commons.scss';
    .num{
        width: 100%;
        position: relative;
        height: 600px;
        background-image: url('../assets/img/counterbg.jpg');
        background-attachment: fixed;
        background-position: center; 
        .num-box{
            width: 70%;
            margin: 0 auto;
            height: 100%;
            .num-card{
                color: white;
                i{
                    font-size: 60px;
                    margin-right: 20px;
                }
                h3{
                    color: #f2b91e;
                    font-family: 'Roboto Slab', serif;
                    font-weight: 600;
                    font-size: 30px;
                }
                span{
                    font-family: 'Roboto Slab', serif;
                    font-size: 20px;
                }
            }
        }
    }
</style>