<template>
  <Navbar />

  <!-- page title -->
  <div class="hidden lg:block container mt-5">
    <div class="page-section">
      <div class="row justify-content-center align-items-center h-100">
        <div class="col-md-6">
          <nav aria-label="Breadcrumb">
            <ul class="breadcrumb justify-content-center py-0 bg-transparent">
              <li class="breadcrumb-item">
                <router-link to="/">Home</router-link>
              </li>
              <li class="breadcrumb-item active">About Me</li>
            </ul>
          </nav>
          <h1 class="text-center">About Me</h1>
        </div>
      </div>
    </div>
  </div>
  
  <Intro />
  <Profile />
  <Services />
  <Personality />
  <!-- TODO: I'll add skills section (technical & soft) -->
  
  <Footer />

  <!-- <Footer :blog="blog" /> -->
</template>

<script>
import Navbar from "../components/Navbar";
import Intro from "../components/Intro";
import Profile from "../components/Profile";
import Services from "../components/Services";
import Personality from "../components/Personality";
import Footer from "../components/Footer";

export default {
  name: "About Page",
  data() {
    return {};
  },

  props: {
    blog: Array,
  },

  components: {
    Navbar,
    Intro,
    Profile,
    Services,
    Personality,
    Footer,
  },
};
</script>

<style></style>
