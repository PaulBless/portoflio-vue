<template>
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
          <!-- We are A Software Company, we must say we're in love 
            with your skills and would liek to discuss a job role with you. Please revert your availability -->
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
