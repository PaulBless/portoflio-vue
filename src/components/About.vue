<template>
  <div class="bg-green-50 page-section pt-5 -mb-5">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 py-3 wow zoomIn">
          <div class="img-place text-center hidden lg:flex">
            <lottie-player
              src="https://assets2.lottiefiles.com/packages/lf20_qhrndegx.json"
              background="transparent"
              speed="1"
              style="max-width: 500px; max-height: 500px"
              autoplay></lottie-player>
          </div>
        </div>

        <div class="col-lg-6 p-4">
          <h2 class="title-section text-2xl">
            All About
            <span class="marked">Paul</span>
          </h2>
          <div class="divider"></div>

          <div>
            <p>
              I am a highly skilled and experienced Software Engineer with a deep understanding of both frontend and backend technologies. 
              With 5+ years of industry experience, I have successfully delivered robust and scalable web applications that meet client requirements and drive business growth.
            </p>
          </div>

          <div>
            <p>
              
            </p>
          </div>

          <div>
            <p class="hidden lg:flex">
              
            </p>
          </div>

          <div class="img-place mb-3"></div>
          <a href="#" class="btn btn-primary">More Details</a>
          <a href="#" class="btn btn-outline border ml-2">Success Stories</a>
        </div>
      </div>
    </div>
    <!-- .container -->
  </div>
  <!-- .page-section -->

  <div class="bg-green-50 page-section">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 p-4 -mt-9 lg:mt-0">
          <h2 class="title-section text-2xl">
            My
            <span class="marked">Skills & Experiences</span>
          </h2>
          <div class="divider"></div>
          <p class="mb-4">
            I graduated from Chonnam National University three months ago with a
            bachelor’s in Computer Engineering. My experiences in school gave me
            strong communication and networking skills, which are crucial for
            event planning.
          </p>
          <p class="mb-4">
            I create successful responsive websites that are fast, easy to use,
            and built with best practices. The main area of my expertise is
            front-end development, HTML, CSS, JS, building small and simple web
            apps,features, animations, and coding interactive. layouts.
          </p>

          <p class="mb-5 hidden lg:flex">
            I also have experiences with building Nft Smart Contract and
            Blockchain Solutions as freelancer developer in South Korea. Since
            beginning my journey as a freelance developer nearly 10 months ago,
            I’ve done remote work for agencies, consulted for startups, and
            collaborated with talented people to create Nfts,Smart Contracts and
            Dapps for both business and consumer use.
          </p>

          <router-link to="/blog" class="btn btn-primary">My Blogs</router-link>
          <router-link to="/projects" class="btn btn-outline ml-2">
            My Projects
          </router-link>
        </div>
        <div class="col-lg-6 py-3 wow zoomIn">
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
    <!-- .container -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      scrollPosition: 0,
    };
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
