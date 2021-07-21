<template>
  <div id="app">
    <Header :api="similApi"/>
    <Jumbotron/>
    <main>
        <Sighature/>
        <NewCourses/>
        <Ad/>
        <Why/>
        <Numbers/>
        <Students/>
    </main>

    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Sighature from './components/Sighature.vue'
import NewCourses from './components/NewCourses.vue'
import Ad from './components/Ad.vue'
import Why from './components/Why.vue'
import Numbers from './components/Numbers.vue'
import Students from './components/Students.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Sighature,
    NewCourses,
    Ad,
    Why,
    Numbers,
    Students,
    Footer
  },
  data(){
        return{
            similApi: [
                {
                    text: 'Courses',
                    new: false,
                    drops: false
                },
                {
                    text: 'Course Formats',
                    new: false,
                    drops: [
                        {
                            link: 'Default Style',
                            styles: false
                        },
                        {
                            link: 'Classic Style',
                            styles: false
                        },
                        {
                            link: 'Udemy Affiliate Style',
                            styles: false
                        },
                        {
                            link: 'Offline Style',
                            styles: false
                        },
                        {
                            link: 'Free Courses',
                            styles: [
                                {
                                    ext: 'Default Style'
                                },
                                {
                                    ext: 'Classic Style'
                                },
                                {
                                    ext: 'Udemy Style'
                                },
                                {
                                    ext: 'Offline Style'
                                },
                            ]
                        },
                        {
                            link: 'Lesson Style 1',
                            styles: false
                        },
                        {
                            link: 'Lesson Style 2',
                            styles: false
                        }
                    ]
                },
                {
                    text: 'Add Courses',
                    new: 'NEW',
                    drops: false
                },
                {
                    text: 'Pages',
                    new: false,
                    drops: [
                        {
                            link: 'About Us',
                            styles: false
                        },
                        {
                            link: 'Shop',
                            styles: false
                        },
                        {
                            link: 'Contact Us',
                            styles: false
                        },
                    ]
                },
                 {
                    text: 'Demos',
                    new: false,
                    drops: [
                        {
                            link: 'Udemy Affiliate',
                            styles: false
                        },
                        {
                            link: 'Light LMS',
                            styles: false
                        },
                        {
                            link: 'Dark LMS',
                            styles: false
                        },
                        {
                            link: 'Offline Courses',
                            styles: false
                        },
                        {
                            link: 'Offline Academy',
                            styles: false
                        },
                        {
                            link: 'Course Hub',
                            styles: false
                        },
                        {
                            link: 'Classic LMS',
                            styles: false
                        },
                        {
                            link: 'Private Instructor',
                            styles: false
                        },
                        {
                            link: 'RTL Demo',
                            styles: false
                        },
                        {
                            link: 'BuddyPress Demo',
                            styles: false
                        },
                        {
                            link: 'Distance Learning',
                            styles: false
                        },
                        {
                            link: 'Cooking Courses',
                            styles: false
                        },
                    ]
                },
                

            ]
        }
    }
}
</script>

<style lang="scss">
  @import '@/style/commons.scss';
  #app {
      position: relative;
      z-index: 300;
      background-color: #fff;
      main{
          background-color: #fff;
          position: relative;
         z-index: 300;
      }
  }
</style>
