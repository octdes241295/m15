<template>
<div id="test">
  <p>{{ message }}</p>
  <button v-on:click="getUser(username)">Send user name to parent</button>
  <h2>User Component</h2>
  <button v-on:click="reverseMessage">Message retourné</button>
    <!-- div 1 -->
  <div class='div10' v-bind:class="[isActive ? 'red' : '']" @click=toggleClass()></div>

  <!-- div 2 -->
  <div class='div10' v-bind:class="[isActive ? 'blue' : 'red']" @click="isActive = !isActive"></div>
  <h1 :class="[isActive ? 'blue' : 'red']">hello</h1>
</div>
</template>

<script>

export default {
  name: 'test',
  data() {
        return {
      message: "bateau",
      isActive: true,
      username:"Peter",
    };
  },
  props: {
    getUser:Function()
  }, 
  methods: {
    reverseMessage() {
      this.message = this.message.split('').reverse().join('')
    },
    toggleClass(){
       this.isActive = !this.isActive;
    }
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.red{
  background: darkgreen;
}

.blue{
  background: blue;
}

.div10{
  width: 100px;
  height: 100px;
  display: inline-block;
  border: 1px solid black;
}
</style>
