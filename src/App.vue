<template>
  <div id="app" class="main">
    <TheHeader 
    :categories="categories"
    />
    <TheMain 
    :developmentCourses="developmentCourses"
    :courses="courses"
    :categories="categories"
    />
  </div>
</template>

<script>
import TheHeader from './components/header/TheHeader.vue'
import TheMain from './components/main/TheMain.vue'
export default {
  name: 'App',
  data(){
    return{
      categories:[
        {name: 'All Categories', icon:'', status: true},
        {name: 'Business', icon:'chart-line', status: false},
        {name: 'Design', icon:'palette', status: false},
        {name: 'Development', icon:'gear',status: false},
        {name: 'IT & Software ', icon: 'terminal', status: false},
        {name: 'Lifestyle', icon: 'face-smile', status: false},
        {name: 'Marketing', icon: 'bullseye', status: false},
        {name: 'Office Productivity', icon: 'print', status: false}
      ],
      courses:[
        {
            title: 'The Complete IOS 10 & Swift 3 Developer Course',
            cover: '895786_7b4b_2-272x161.jpg',
            category: 'Development',
            sale: 50,
            price: 199.99,
            rank: 4
        },
        {
            title: 'CSS - The Complete Guide 2020 (incl. Flexbox, Grid & Sass)',
            cover: '1561458_7f3b-272x161.jpg',
            category: 'Design',
            sale: 50,
            price: 199.99,
            rank: 5
        },
        {
            title: 'Web Design for Beginners: Real World Coding in HTML & CSS',
            cover: '246154_d8b0_3-272x161.jpg',
            category: 'Development',
            sale: 50,
            price: 129.99,
            rank: 5
        },
        {
            title: 'Digitally Painting Light and Color: Amateur to Master',
            cover: '1208228_d61c_4-272x161.jpg',
            category: 'Design',
            sale: 50,
            price: 139.99,
            rank: 4
        },
        {
            title: 'Become an Arabic Calligraphy Artist from Scratch',
            cover: '186792_41e4_4-272x161.jpg',
            category: 'Art & Crafts',
            sale: 0,
            price: 199.99,
            rank: 5
        },
        {
            title: 'Google Searchin Ninja',
            cover: '1776542_30b1-272x161.jpg',
            category: 'Google',
            sale: '50',
            price: 199.99,
            rank: 4
        },
        {
            title: 'Foundations for Mastering Watercolor Painting',
            cover: '949316_2a64_11-272x161.jpg',
            category: 'Art & Crafts',
            sale: 50,
            price: 19.99,
            rank: 5
        },
        {
            title: 'Get Wine-Smart',
            cover: '366802_6fcc-272x161.jpg',
            category: 'Food & Beverage',
            sale: 50,
            price: 49.99,
            rank: 5
        },
        {
            title: 'GitHub Ultimate: Master Git and GitHub - Beginner to Expert',
            cover: '752950_b773-272x161.jpg',
            category: 'Development',
            sale: 50,
            price: 99.99,
            rank: 4
        },
        {
            title: 'The Colored Pencil Drawing Course',
            cover: '381588_2e6d_4-272x161.jpg',
            category: 'Art & Crafts',
            sale: 50,
            price: 34.99,
            rank: 5
        },
        {
            title: 'Paint Realistic Watercolor and Botanicals - STUDIO BASICS',
            cover: '838056_611a_3-272x161.jpg',
            category: 'Art & Crafts',
            sale: 50,
            price: 69.99,
            rank: 4
        },
        {
            title: 'Mastering Brushstrokes - Part 1',
            cover: '1414956_d944_15-272x161.jpg',
            category: 'Art & Crafts',
            sale: 50,
            price: 19.99,
            rank: 5
        },
        {
            title: 'Paint Realistic Watercolor and Botanicals - MAGNOLIAS',
            cover: '1109398_4c13-272x161.jpg',
            category: 'Art & Crafts',
            sale: 50,
            price: 69.99,
            rank: 4
        },
        {
            title: 'The Complete IOS 11 & Swift Developer Course - Build 20 Apps',
            cover: '1253188_58f7_2-272x161.jpg',
            category: 'Development',
            sale: 50,
            price: 199.99,
            rank: 4
        },
        {
            title: 'Android Java Masterclass - Become an App Developer',
            cover: '919872_ed54_6-272x161.jpg',
            category: 'Development',
            sale: 50,
            price: 99.99,
            rank: 5
        },
        {
            title: 'Xamarin Forms: Build Native Cross-platform Apps with C#',
            cover: '951684_9c1a_2-272x161.jpg',
            category: 'Development',
            sale: 50,
            price: 189.99,
            rank: 4
        }
      ],
      developmentCourses:[],
    }
  },
  components:{
    TheHeader,
    TheMain
  },
  created(){
    this.courseActualPrice()
    this.filterDevelopmentCourses()
    this.activeCategory()
  },
  methods:{
    courseActualPrice(){
        let actualPrice = null
        let percentage = null
        for (let i = 0; i < this.courses.length; i++){
            if (this.courses[i].sale > 0){
                percentage = (this.courses[i].price * this.courses[i].sale) / 100
                actualPrice = Math.ceil(this.courses[i].price - percentage)
                this.courses[i].actualPrice = actualPrice
            }
        }
        return
    },
    filterDevelopmentCourses(){
      this.courses.forEach(course => {
        if (course.category.toLocaleLowerCase() == 'development'){
          this.developmentCourses.push(course )
        }
      })
      console.log(this.developmentCourses)
      return this.developmentCourses
    },
    activeCategory(){
      this.categories.forEach(category => {
        if (category.status){
          category.class = 'active'
        }
      })
    }
  }
}
</script>

<style lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

</style>
