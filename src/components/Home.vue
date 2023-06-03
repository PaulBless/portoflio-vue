<template>
  <Navbar />
  <Header />
  <Services />
  <Intro />
  <Personality />

  <!-- <ContactForm /> -->
  <!-- <Blog :blog="blog" /> -->
  
  <Footer />
</template>

<script>
import Navbar from "./Navbar.vue";
import Header from "./Header.vue";
import Services from "./Services.vue";
import Intro from "./Intro.vue";
import Projects from "./Projects.vue";
import Contact from "./Contact.vue";
import Blog from "./Blog.vue";
import Personality from "./Personality.vue";
import ContactForm from "./ContactForm.vue";
import Footer from "./Footer.vue";

export default {
  name: "Home",
  data() {
    return {};
  },

  props: {
    blog: Array,
  },

  components: {
    Navbar,
    Header,
    Services,
    Intro,
    Projects,
    Contact,
    Blog,
    Personality,
    ContactForm,
    Footer,
  },
};
</script>

<style></style>
