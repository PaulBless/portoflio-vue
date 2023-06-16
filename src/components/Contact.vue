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
          <h1 class="text-center">I'd love to hear from you.</h1>
        </div>
      </div>
    </div>
  </div>

  <!-- <ContactForm /> -->


  <!-- copy -->
  <div class="container">
    <div class="row align-content-center page-section">
        <div class="contact col-lg-6 py-3 addr">
          <h3 class="title-section">Let's <span class="marked">Start</span> Something Great!</h3>
          <div class="divider"></div>
          <p>
            Great genius takes shape by contact with another great genius,
            but, less by assimilation than by friction. I believe we're evaluated 
            and classified by these four contacts: what we do, how we look, what we say, and how we say it.
          </p>
          <p>
            I'm ready to give real service, and in my quest to achieve that, I strive to add something which cannot 
            be bought or measured with money; <em><strong>sincerity</strong></em> and <em><strong>integrity</strong></em>. 
          </p>
          <p>
            Need to get in touch with me? Complete the quick form. 
            Your message will be confidently sent to my email. 
            If forms aren't your thing, book an appointment with me using 
            this link <a class="book" href="https://calendly.com/eshunbless1" target="_blank">Calendly</a> .</p>
        </div>

        <div class="touch col-lg-6 py-3">
          <h3 class="title-section">Get in Touch</h3>
          <div class="divider"></div>
          <p class="mb-3">Please fill the form below and I'll respond quickly.</p>
          <form class="contactform" @submit.prevent="handleFormSubmit">
            <div class="row">
              <div class="col-12 col-lg-6">
                <div class="form-group">
                  <input
                    class="f-input"
                    type="text"
                    v-model="name"
                    placeholder="Name"
                    name="name"
                    required
                    aria-required="true"
                  />
                </div>
              </div>
              <div class="col-12 col-lg-6">
                <div class="form-group">
                  <input
                    class="f-input"
                    type="email"
                    v-model="email"
                    placeholder="Email address"
                    name="email"
                    required
                    aria-required="true"
                  />
                </div>
              </div>
              <div class="col-12 col-lg-12">
                <div class="form-group">
                  <input
                    class="f-input"
                    type="text"
                    v-model="subject"
                    placeholder="Message Subject"
                    name="subject"
                    required
                    aria-required="true"
                  />
                </div>
              </div>
              <div class="col-12">
                <div class="form-group">
                  <textarea
                    class="f-input"
                    v-model="message"
                    placeholder="Message details"
                    rows="5"
                    name="message"
                    aria-required="true"
                  ></textarea>
                </div>
              </div>
              <div class="col-12">
                <!-- error message -->
                <div v-if="response" class="alert alert-danger mt-3 mb-0">{{response}}</div>
                <label v-if="success" class="alert alert-success m-2">{{ success }}</label>

                <button :disabled="isLoading">
                  <div v-if="isLoading">
                    <span>sending...</span>
                    <span
                      class="spinner-border spinner-border-sm mr-1"
                    ></span>
                  </div>
                  <div v-else>
                    <span class="btn-text">Send Message </span>
                    <i class="mai-paper-plane btn-icon"></i>
                  </div>
                </button>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  <!-- end -->

  

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
  data() {
    return {
      name: "",
      email: "",
      subject: "",
      message: "",
      isLoading: false,
      response: '',
      success: '',
      instagramLogo: require("@/assets/img/svg/instagram.svg"),
      twitterLogo: require("@/assets/img/svg/twitter.svg"),
      linkedinLogo: require("@/assets/img/svg/linkedin.svg"),
      gitHubLogo: require("@/assets/img/svg/github.svg"),
    };
  },
  methods: {
    
    handleFormSubmit() {
      this.isLoading = true;
      fetch("https://formsubmit.co/ajax/eshunbless1@gmail.com", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
          Accept: "application/json",
        },
        body: JSON.stringify({
          name: this.name,
          email: this.email,
          subject: this.subject,
          message: this.message,
        }),
      })
        .then((response) => response.json())
        .then((data) => {
          console.log(data);
          this.success = data.message + " Thank you for reaching out, I'll revert soon!"
          this.name = "";
          this.subject = "";
          this.message = "";
          this.email = "";
          this.isLoading = false;
        })
        .catch((error) => {
          console.log(error);
          this.isLoading = false;
          this.response = error.message;
        });
    },
  },
};
</script>

<style scoped>
.form-control:focus {
  box-shadow: none !important;
  border-color: #f31c4d !important;
}
.book {
  color: #35bb78 !important;
  text-decoration: underline;
}
.book:hover{
  color: #f31c4d !important;
  text-decoration: none;
}
/* style */
.contact > p {
  margin-bottom: 1.5rem;
}
 .contact > h3, .touch> h3 {
  font-size: 26px;
}
 
 .row > * {
  padding-left: 15px;
  padding-right: 15px;
}
 .contactform .form-group {
  margin-bottom: 25px;
}
 .contactform input[type="text"], .contactform input[type="email"] {
  background-color: #fff;
  border: 1px solid #ddd;
  color: #666;
  width: 100%;
  padding: 11px 26px;
  border-radius: 10px;
  outline: none !important;
  transition: 0.3s;
}
 /* .contactform input[type="text"]:focus, .contactform input[type="email"]:focus {
  border: 1px solid #35bb78 !important;
  box-shadow: none !important;
  
} */
 .contactform textarea {
  border: 1px solid #ddd;
  width: 100%;
  padding: 12px 26px;
  height: 120px;
  overflow: hidden;
  border-radius: 10px;
  outline: none !important;
  transition: 0.3s;
  resize: none;
}
 .contactform .f-input:focus {
	border: 1px solid #35bb78 !important;
  box-shadow: none !important;
}
 
.contactform button {
  overflow: hidden;
  text-align: center;
  cursor: pointer;
  vertical-align: middle;
  -webkit-user-select: none;
  -moz-user-select: none;
  user-select: none;
  background-image: linear-gradient(to right, #198754, #198754 50%, transparent 50%, transparent);
  background-position: -100% 0;
  background-size: 200% 100%;
  transition: all 0.5s ease-out;
  text-transform: capitalize;
  text-decoration: none !important;
  position: relative;
  z-index: 1;
  font-size: 15px;
  font-weight: 600;
  background-color: transparent;
  outline: none !important;
  cursor: pointer !important;
  margin: 0;
  font-family: inherit;
  position: relative;
  border: 1px solid #198754;
  display: inline-block;
  line-height: 1.4;
  border-radius: 50px;
  white-space: nowrap;
  text-overflow: ellipsis;
  padding: 16px 60px 16px 20px;
  vertical-align: middle;
  color: #198754;
  text-align: center;
  -webkit-appearance: none;
  -moz-appearance: none;
}
 .contactform button .btn-text {
  position: relative;
}
 .contactform button .btn-icon {
  box-sizing: border-box !important;
  position: absolute;
  right: -1px;
  top: -1px;
  bottom: 0;
  width: 55px;
  height: 55px;
  /* padding: 1rem; */
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  border-radius: 50%;
  background-color: #198754;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
}
 .contactform button::before {
  z-index: -1;
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  transform: translateX(100%);
  transition: all 0.3s ease-out;
}
 .contactform button:hover {
  background-position: 0 0;
  color: white;
}
 .contactform .btn-icon {
  width: 50px;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 15px;
}
 .primary {
  font-size: 0.9rem;
  padding: 0.5rem 1rem;
}
 
</style>
