<template>
  <div id="jumbo-box">
      <img :src="require('@/assets/img/jumbo.jpg')" alt="jumbo">
        <!-- immagine e scritta -->
        <div id="int-jumbo">
            <h2 >Start your Human <br> <span class="text-yellow">Revolution</span>  today</h2>
            <div class="p-box">
                <p>A wonderful serenity has taken possession of my entire soul, like these sweet mornings of spring which I enjoy with my whole heart.</p>
            </div>
        </div>
        <!-- countdown -->
        <div class="d-flex justify-content-around count-box">
            <div>
                <h3> <span class="text-white">Limited Sale:</span> All courses with 55% off</h3>
                <div>
                    <input placeholder="Enter Your E-mail" type="email">
                    <button>SUBSCRIBE</button>
                </div>
            </div>
            <div class="d-flex">
                <div class="form-c">
                    <span>{{days}}</span>
                    <h4>Days</h4>
                </div>
                <div class="form-c">
                    <span>{{hours}}</span>
                    <h4>Hours</h4>
                </div>
                <div class="form-c">
                    <span>{{minutes}}</span>
                    <h4>Minutes</h4>
                </div>
                <div class="form-c">
                    <span>{{seconds}}</span>
                    <h4>Seconds</h4>
                </div>
            </div>
        </div>
  </div>
</template>

<script>

export default {
    name: 'Jumbotron',
    data(){
       return{
           days :'',
           hours :'',
           minutes :'',
           seconds :'',
           countDownDate : new Date("Jan 5, 2022 15:37:25").getTime(),
           time : 'ciao',
           intervalid:''
        }
    },
    methods: {

       
        todo(){
            this.intervalid = setInterval(() => {
            var now = new Date().getTime();
            this.time = this.countDownDate - now
            var days = Math.floor(this.time / (1000 * 60 * 60 * 24));
            var hours = Math.floor((this.time % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((this.time % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((this.time % (1000 * 60)) / 1000);
            this.days = days;
            this.hours = hours;
            this.minutes = minutes;
            this.seconds = seconds;
        }, 1000)}
        
        
    },
    mounted(){
        this.todo()
        // this.setInterval(function(){ console.log(this.time) }, 3000);
    }
}

</script>

<style lang="scss" scoped>
@import '@/style/commons.scss';
#jumbo-box {
    position: relative;
    #int-jumbo {
        position: absolute;
        left: 50%;
        top: 30%;
        h2 {
            font-family: 'Roboto Slab', serif;
            font-size: 70px;
            font-weight: 700;
            line-height: 70px;
        }
        .p-box {
            width: 600px;
            p {
                font-size: 18px;
            }
        }
        
    }
    .count-box{
        background-color: #f2b91e;
        border-radius: 20px;
        width: 80%;
        padding: 50px;
        position: absolute;
        bottom: -10%;
        left: 50%;
        transform: translate(-50%, 0%);
        h3 {
            font-family: 'Roboto Slab', serif;
            line-height: 38px;
            letter-spacing: -0.5px;
            font-size: 34px;
        }
        input {
            padding: 6px 70px 6px 25px;
            height: 60px;
            width: 500px;
            border: none;
            border-radius: 30px;
            box-shadow: 0 5px 10px 0 rgba(0,0,0,.1);
            margin-top: 30px;
            &:focus {
                outline: none;
            }
        }
        button {
            background-color: #2d4649;
            color: white;
            border: none;
            height: 60px;
            border-radius: 30px;
            padding: 10px;
            margin-left: -60px;
        }
        .form-c{
            margin: 0 20px;
            text-align: center;
            span {
                color: white;
                font-size: 60px;
                font-weight: 600;
            }
            h4 {
                font-weight: 600;
            }
        }
    }
}

</style>