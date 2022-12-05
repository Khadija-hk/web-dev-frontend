<template>
  <div class="container">
    <!-- S3: Use the component  -->
    <PhoneTop webpageTitle="Google pixel phone models" />
    <PhoneBox :phones="phones" />
  </div>

</template>

<script>
//S1: Import the component
import PhoneTop from './components/PhoneTop.vue'
import PhoneBox from './components/PhoneBox.vue'

export default {
  name: 'App',

  //S2: Register the component
  components: {
    PhoneTop,
    PhoneBox
  },

  data() {
    return {
      phones: []
    }
  },

  methods: {
    async fetchphones() {
      const res = await fetch("https://khadija-portfolio.onrender.com/api")
      const data = await res.json()
      console.log(data.phones)

      return data.phones
    }
  },

  async created() {
    this.phones = await this.fetchphones()
  }
}

</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.2em solid black;
  padding: 30px;
  border-radius: 2px;
}

div {
  margin-bottom: 0.5em;
}
</style>