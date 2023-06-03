<template>

  <div class="bg-green-50 page-section">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 p-4 -mt-9 lg:mt-0">
          <h2 class="title-section text-2xl" data-aos="slide-right">
            Profile <span class="marked">Summary</span>
          </h2>
          <div class="divider"></div>
          
          <p class="mb-4 " data-aos="fade-up">
            I hold a Bachelor’s Degree in Computer Science from Valley View University, Ghana. 
            My experiences in school and research projects gave me strong communication, collaboration and networking skills, 
            which are integral to my work style.
          </p>
          
          <p class="mb-4 " data-aos="fade-up">
            On the frontend, I excel in HTML, CSS, and JavaScript, along with popular frontend frameworks such as React and Vue.js. 
            I have a keen eye for detail and a strong focus on creating intuitive and engaging user interfaces. 
            I employ responsive design principles to ensure that applications look and function flawlessly across different devices and screen sizes.
            
          </p>

          <p class="mb-4 " data-aos="fade-up">
            In backend development, I'm proficient in PHP and JavaScript frameworks including Laravel and Express. I can employ them to build powerful and efficient server-side logic. 
            I have a solid understanding of database management systems, such as MySQL and MongoDB, and can design and optimize complex database structures. 
            Additionally, I have experience working with RESTful APIs, integrating third-party services, and implementing secure authentication and authorization systems.
            
          </p>

          <p class="mb-4 " data-aos="fade-up">
            I possess a blend of unique traits and qualities that equip me to create innovative and 
            efficient web applications that drive business success while providing an exceptional user experience.
          </p>

          <!-- TODO: Reactivate buttons after working on respective pages-->
          <!-- <router-link to="/blog" class="btn btn-primary">My Blogs</router-link> -->
          <!-- <router-link to="/projects" class="btn btn-outline ml-2">My Projects </router-link> -->
        </div>
        <div class="col-lg-6 py-3 " data-aos="zoom-in">
          <div class="img-place text-center">
            <lottie-player
              src="https://assets2.lottiefiles.com/packages/lf20_u4jjb9bd.json"
              background="transparent"
              speed="0.5"
              style="max-width: 550px; max-height: 550px"
              loop
              autoplay></lottie-player>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- <Personality /> -->
  <!-- .container -->
</template>

<script>
import Intro from './Intro.vue';
import Personality from './Personality.vue';

export default {
  data() {
    return {
      scrollPosition: 0,
    };
  },
  components:{
    Intro,
    Personality,
  },

  methods: {
    handleScroll(e) {
      this.scrollPosition = e.target.scrollTop;

      if (this.scrollPosition > 100) {
        console.log("UP");
      } else {
        console.log("DOWN");
      }
    },
  },
};
</script>

<style scoped>
.marked{
  /* color: #55f978; */
  /* color: #35bb78; */
  /* color: #198754; */
}
</style>
