<template>  
  <div class="">

  <Navbar />

  <!-- page title -->
  <div class="hidden lg:block container mt-0">
    <div class="page-banner1">
      <div class="row justify-content-center align-items-center h-100">
        <div class="col-md-6">
          <nav aria-label="Breadcrumb">
            <ul class="breadcrumb justify-content-center py-0 bg-transparent">
              <li class="breadcrumb-item">
                <router-link to="/">Home</router-link>
              </li>
              <li class="breadcrumb-item active">Projects</li>
            </ul>
          </nav>
          <h1 class="text-center">Take a look of some of my works!</h1>
          <p class="text-center">          
            I bring a comprehensive skill set, a strong work ethic, and a passion for delivering high-quality solutions to every project I undertake. 
          </p>
        </div>
      </div>
    </div>
  </div>

  <div class="hidden lg:block lg:items-center lg:justify-center mt-0" style="display: none;">
    <div class="page-banner1 p-5">
      <div class="container">
        <div class="row justify-content-center align-items-center">
          I bring a comprehensive skill set, a strong work ethic, and a passion for delivering high-quality solutions to every project I undertake. 
        </div>
      </div>
    </div>
  </div>
    
    <div class="page-section bg-green-50">
      <div class="container">
        <div class="row my-5 card-blog-row">
          <div class="relative lg:hidden col-md-6 col-lg-3 py-3 " data-aos="fade-up">
            <div class="card-blog">
              <div class="header">
                <div class="entry-footer">
                  <div class="post-author">Welcome to my projects</div>
                </div>
              </div>
              <div class="body">
                <div class="post-title">
                  <a>
                    My Knowledge Area
                    <br />
                    Research Skills
                    <br />
                    Clients Projects
                  </a>
                </div>
              </div>
            </div>
          </div>

          <div
            v-for="(a, i) in project"
            :key="a"
            class="col-md-5 col-lg-4 py-5 px-4">
            <div
              class="flex flex-col space-y-5 border shadow-md border-green-500 bg-white h-96 rounded-md hover:-mt-1 hover:shadow-lg hover:shadow-green-200 cursor-pointer">
              <div
                class="flex items-center justify-center -mt-6 h-48 rounded-t-lg overflow-hidden">
                <img class="h-48 w-96 rounded-t-lg" :src="project[i].image" />
              </div>

              <div class="flex flex-col ml-4">
                <div class="text-xl font-medium text-green-600 ml-3 mb-2">
                  <a>{{ project[i].name }}</a>
                </div>
                <div
                  class="text-base h-18 lg:h-12 text-gray-700 ml-3 mr-3 mb-5">
                  {{ project[i].content }}
                </div>

                <div
                  class="flex flex-row items-start py-3 px-2 space-x-3 ml-2"
                  style="padding-bottom: 25px">
                  <img :src="project[i].tech1" />
                  <img :src="project[i].tech2" />
                  <img :src="project[i].tech3" />
                </div>
              </div>
            </div>
            <div class="mt-4 hover:underline">
              <a
                :href="project[i].live"
                class="btn text-lg hover:bg-green-100 hover:underline hover:font-medium">
                Live
                <span class="mai-chevron-forward text-sm"></span>
              </a>

              <a
                :href="project[i].code"
                class="btn text-lg hover:bg-purple-100 hover:font-medium">
                Source Code
                <span class="mai-chevron-forward text-sm"></span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script>

import ProjectData from "../data/works.js";

import Navbar from "../components/Navbar";
import Services from "../components/Services";
import Footer from "../components/Footer";

export default {
  name: "Project Page",
  data() {
    return {
      project: ProjectData,
    };
  },

  props: {
    blog: Array,
  },

  components: { Navbar, Services, Footer },
};
</script>

<style></style>
