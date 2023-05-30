<template>
  <header>
    <div class="page-banner home-banner">
      <div class="container h-100">
        <div class="row align-items-center h-100">
          <div class="col-lg-6 py-3 wow fadeInUp">
            <p
              class="text-green-600 hover:text-green-500 text-2xl lg:text-4xl font-medium lg:font-semibold mb-5 lg:leading-normal leading-snug">
              Hi, I'm PAUL
              <br />
              Full Stack Developer,
              <br />
              API Developer
            </p>
            <p
              class="hidden lg:block text-2xl mb-5">
              I focus to deliver robust and scalable 
              web applications that meet client requirements 
              and drive business growth.
            </p>

            <router-link
              to="/about"
              name="fade"
              class="btn btn-outline border-success text-secondary link">
              About
            </router-link>
            <a
              href="https://drive.google.com/file/d/1uNPJABGXLZAcEXE5ZqFJVyP-r_6dljmF/view?usp=drive_link"
              target="_blank"
              class="btn btn-success btn-split ml-2 link">
              Resume
              <div class="fab"><span class="mai-play"></span></div>
            </a>
          </div>
          <div class="col-lg-6 wow zoomIn">
            <div
              class="m-3 lg:m-3 p-1 lg:p-5">
              <lottie-player
                src="https://assets2.lottiefiles.com/packages/lf20_gnb0jsok.json"
                background="transparent"
                speed="1"
                style="max-width: 500px; max-height: 500px"
                autoplay></lottie-player>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import { directive as motion } from "@vueuse/motion";

export default {};
</script>

<style></style>
