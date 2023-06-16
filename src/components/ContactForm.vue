<template>
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
              <div class="content"><a href="#">eshunbless1@gmail.com</a></div>
            </li>
            <li>
              <div class="icon"><span class="mai-phone-portrait"></span></div>
              <div class="content"><a href="#">+233 241 565 520</a></div>
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
            </button>
          </div>
          </form>
        </div>
      </div>
    </div>
    <!-- .container -->
  </div>
    <div class="container">
      <form ref="form" @submit.prevent="sendEmail1">
        <label>Name</label>
        <input 
          type="text" 
          v-model="name"
          name="user_name"
          placeholder="Your Name"
          required
        >
        <label>Email</label>
        <input 
          type="email" 
          v-model="email"
          name="user_email"
          placeholder="Your Email"
          required
          >
        <label>Message</label>
        <textarea 
          name="message"
          v-model="message"
          cols="30" rows="5"
          placeholder="Message" required>
        </textarea>
        <input type="submit" value="Send">
      </form>
    </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  name: 'ContactForm',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    sendEmail1() {
      emailjs.sendForm('service_0revyqo', 'template_udy96jx', this.$refs.form, 'jdLkCpYYML_zJsZ4q')
        .then((result) => {
            console.log('SUCCESS!', result.text);
        }, (error) => {
            console.log('FAILED...', error.text);
        });
    },
    sendEmail(e) {
      try {
        emailjs.sendForm('service_0revyqo', 'template_udy96jx', e.target, 'jdLkCpYYML_zJsZ4q', {
          from_name: this.name,
          from_email: this.email,
          message: this.meessage
        })

        alert("email sent");

      } catch (err) {
        console.log(err);
           if (err instanceof ReferenceError) {
            alert( "JSON Error: " + err.message );
           } else {
            throw err; // rethrow
           }
      }
      
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
}
</script>

<style scoped>
* {box-sizing: border-box;}

label {
  float: left;
}
input[type=text], [type=email], textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

input[type=submit] {
  background-color: #4CAF50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #b8c7b9;
}

.container {
  display: block;
  margin:auto;
  text-align: center;
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
  width: 50%;
}
</style>
