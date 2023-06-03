<template>
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
              <li class="breadcrumb-item active">Contact Me</li>
            </ul>
          </nav>
          <h1 class="text-center">I'd love to hear from you</h1>
          
        </div>
      </div>
    </div>
  </div>

  <ContactForm />

  <div class="page-section">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 py-3 " data-aos="fade-up">
          <h2 class="title-section">Contact Information</h2>
          <div class="divider"></div>
          <p>
            Great genius takes shape by contact with another great genius,
            <br />
            but, less by assimilation than by friction. - Heinrich Heine
          </p>

          <ul class="contact-list">
            <li>
              <div class="icon"><span class="mai-map"></span></div>
              <div class="content">123 Main Street, Seoul, South Korea</div>
            </li>
            <li>
              <div class="icon"><span class="mai-mail"></span></div>
              <div class="content"><a href="#">aaron08889@gmail.com</a></div>
            </li>
            <li>
              <div class="icon"><span class="mai-phone-portrait"></span></div>
              <div class="content"><a href="#">+233</a></div>
            </li>
          </ul>
        </div>
        <div class="col-lg-6 py-3" data-aos="fade-up">
          <h2 class="title-section">Get In Touch</h2>
          <div class="divider"></div>
          <p>I'd love to hear from you. Please fill below form.</p>
          <form action="#">
            <div class="py-2">
              <input type="text" class="form-control" placeholder="Name" />
            </div>
            <div class="py-2">
              <input type="text" class="form-control" placeholder="Email address" />
            </div>
            <div class="py-2">
              <textarea rows="6" class="form-control" placeholder="Enter message"></textarea>
            </div>
            <div class="py-2">
            <button type="submit" class="btn btn-primary rounded-pill mt-4">
              Send Message
            </button></div>
          </form>
        </div>
      </div>
    </div>
    <!-- .container -->
  </div>

  <Footer />
</template>

<script>
import Navbar from "./Navbar.vue";
import ContactForm from "./ContactForm.vue";
import Footer from "./Footer.vue";

export default {
  name: "Contact",

  components: {
    Navbar: Navbar,
    ContactForm: ContactForm,
    Footer: Footer,
  },
};
</script>

<style scoped>
.form-control:focus {
  box-shadow: none !important;
  border-color: #f31c4d !important;
}
</style>
