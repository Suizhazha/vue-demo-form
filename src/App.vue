<template>
  <div id="app">
    <label>
      <input v-model="message" placeholder="edit me">
    </label>
    <p>Message is: {{ message }}</p>
    <p><button @click="message = 'suixin'"> set message to suixin</button></p>
  </div>
</template>

<script>
export default {
  name: "App",
  data(){
     return {
       message:'hi'
     }
  },
  components: {
  }
}
</script>

