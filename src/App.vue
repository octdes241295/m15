<template>
  <div id="app">
    <HelloWorldBis :msg="msg1" :gethid="getishid" :ishid1="ishid1"/>
    <HelloWorldBis1  :msg="msg1" :gethid1="getishid1" :ishid="ishid"/>

  </div>
</template>

<script>
import HelloWorldBis from "./components/HelloWorldBis.vue";
import HelloWorldBis1 from "./components/HelloWorldBis1.vue";

export default {
  name: "App",
  data() {
    return {
      msg1: "sehtr",
      msg2: "uhdfuh",
      name: "gogo",
      ishid: false,
      ishid1: false,
    };
  },

  components: {
    HelloWorldBis,
    HelloWorldBis1,
  },
  methods: {
    handleClick() {
      this.msg1 = "ohoh";
      this.msg2 = "ahah";
    },
    getUsername(name) {
      this.name = name;
    },
    getishid(ishid){
      this.ishid=ishid
    },
    getishid1(ishid1){
      this.ishid1=ishid1
    }
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  height: 100%;
  display: grid;
  grid-template-columns: auto;
  background-color:rgb(138, 117, 47);
}

</style>
