<template>
    <div class="container">
        <div class="col-lg-5">
            <calendly-vue url="eshunbless1" @event="logEvent" @event-details="logEvent" @error="logEvent"></calendly-vue>
        </div>
    </div>
</template>

<script>
import CalendlyVue from "calendly-vue"

export default {
  name: 'CalendlyVue',
  data() {
    return {
    }
  },
  methods: {
    logEvent(evt) {
        console.log(evt)

        // Here you can handle the emitted events with custom code
        if (evt === "calendly.profile_page_viewed") {
            console.log("Calendly profile has been opened")
            }
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
