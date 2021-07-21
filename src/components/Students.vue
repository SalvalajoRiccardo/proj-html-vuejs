<template>
    <div id="students">
        <h2>What Students Say</h2>
        <div class="slider-top d-flex justify-content-center align-items-center">
            <button @click="prevAlbum()"><i class="fas fa-arrow-left"></i></button>
            
            <div v-for="(stu, index) in people" :key="index">
                <img @click="change(index)" :class="(index == contatore) ? 'focus' : ''" :src="stu.iga" alt="student">
            </div>
            
            <button @click="nextAlbum()"><i class="fas fa-arrow-right"></i></button>
        </div>
        <div class="slider-bot">
            <div :class="(index == contatore) ? 'active' : 'none'" v-for="(stu, index) in people" :key="index">
                <h3>{{stu.tit}}</h3>
                <div>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                </div>
                <p>{{stu.par}}</p>
            </div>
        </div>

    </div>
</template>

<script>
import img1 from '../../public/assets/img1.jpg'
import img2 from '../../public/assets/img2.jpg'
import img3 from '../../public/assets/img3.jpg'

export default {
    name:'Students',
    data(){
        return{
            contatore: 0,
            people: [
                {
                    iga: img1,
                    tit: "Come as you are",
                    par: "MasterStudy used is an excellent workshop whether you come as a counselor, advisor, administrator, or faculty member. I am going home empowered. I am looking forward to attending the On Course MasterStudy and the MasterStudy National Conference next year and facilitating the use of this excellent retention/student success course at my college."
                },
                {
                    iga: img2,
                    tit: " Paints of the Future",
                    par:" The response to your MasterStudy has been really overwhelming! Those who participated in the workshop are spreading the word here on campus and the “buzz” is on. The VP of Instruction wants you to come back! Her goal is to have more faculty trained. She also wants to attend a workshop herself. Our President told me Masterstudy needs to be the cornerstone of our success program."
                },
                {
                    iga: img3,
                    tit: "Investing for Your Future",
                    par:"It is no exaggeration to say this MasterStudy experience was transformative–both professionally and personally. This workshop will long remain a high point of my life. Thanks again…. I am feeling energized and eager to start teaching my class next week. I can’t wait to use all of my new teaching tools. I will absolutely recommend this workshop to other educators!"
                }
            ]
        }
    },
    methods: {
        nextAlbum() {
            this.contatore++;
            if (this.contatore > this.people.length - 1){
                this.contatore = 0;
            }
        },
        prevAlbum() {
            this.contatore--;
            if (this.contatore < 0){
                this.contatore = this.people.length - 1;
            } 
        },
        change(i) {
            this.contatore = i;
            console.log(this.contatore);
        },
    },
    mounted() {
        setInterval(this.nextAlbum, 10000);
    }
    
}
</script>

<style lang="scss" scoped>
    .focus{
        transform: scale(1.3);
    }
    .active{
        display: block;
    }
    .none{
        display: none;
    }
    #students{
        text-align: center;
        width: 50%;
        margin: 0 auto 300px;
        background-color: #fff;
        padding-bottom: 100px;
        h2{
            font-family: 'Roboto Slab', serif;
            font-weight: 600;
            font-size: 50px;
            margin: 100px 0;
        }
        .slider-top{
            margin-bottom: 50px;
            button{
                border: none;
                background-color: #fff;
                font-size: 30px;
            }
            img{
                margin: 0 30px;
                border-radius: 50%;
                width: 70px;
            }
        }
        .slider-bot{
            margin-bottom: 50px;
            i{
                color: #f2b91e;
                margin: 0 2px;
            }
            h3{
                font-family: 'Roboto Slab', serif;
                font-weight: 600;
                font-size: 25px;
            }
            p{
                margin: 20px auto 0;
                line-height: 35px;
                font-family: 'Roboto Slab', serif;
                font-size: 20px;
                width: 770px;
            }
        }
    }
</style>