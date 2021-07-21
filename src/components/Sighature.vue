<template>
  <div class="sign-box d-flex justify-content-around">
      <div id="sign">
        <h2>Hey there, my name is John Doe. I'm the founder of the Brain Academy. 
        </h2>
        <img :src="require('@/assets/img/sign.jpg')" alt="sign">
      </div>
      <div class="text">
        <p>
          A wonderful serenity has taken possession of my entire soul, like these sweet mornings of spring which I enjoy with my whole heart. I am alone, and feel the charm of existence in this spot, which was created for the bliss of souls like mine. I am so happy, my dear friend, so absorbed in the exquisite sense of mere tranquil existence, that I neglect my talents. When, while the lovely valley teems with vapour around me, and the meridian sun strikes the upper surface of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary
        </p>
      </div>
  </div>
</template>

<script>
export default {
name: 'Sighature'
}
</script>

<style lang="scss" scoped>
@import '@/style/commons.scss';
.sign-box {
    width: 70%;
    margin: 0 auto 100px;
    padding-top: 100px;
    background-color: #fff;
    h2{
      font-family: 'Roboto Slab', serif;
      font-size: 36px;
      font-weight: 700;
      line-height: 50px;
      margin-top: 100px;
    }
    .text {
      width: 50%;
      padding: 0 50px 0 0;
      p{
        font-size: 18px;
        line-height: 30px;
        margin-top: 100px;
      }
    }
    #sign{
      width: 50%;
      padding: 0 100px 0 0;
      img{
        margin-top: 50px;
        margin-left: 200px;
      }
    }
}
</style>