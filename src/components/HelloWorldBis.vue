
<template>
  <div class="div" v-bind:class="ishid1 ? 'hidden' : ''">
    <div class="div1">
      <div class="divi">
      <div class="h3 m-1">
        <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
      </div>
      <div style="margin-left:10px">Editor</div>
      </div>
      <div class="h3 m-1">
        <button class="btn" @click="toggleClass()" v-on:click="gethid(ishid)"><b-icon-aspect-ratio-fill></b-icon-aspect-ratio-fill></button>
      </div>
    </div>
    <div class="font" :class="[isActive ? 'div2' : 'div2bis']">
      <p>
      # Welcome to my React Markdown Previewer!0<br><br>

      ## This is a sub-heading...<br>
      ### And here's some other cool stuff:<br><br>

      Heres some code, <code>'div div'</code> between 2 backticks.<br><br>

      ```<br>
      // this is multi-line code:<br><br>

      <code>function anotherExample(firstLine, lastLine) {<br>
      if (firstLine == '```' " lastLine == '```') {<br>
          return multiLineCode;<br>
        }<br>
      }<br>
      ```</code><br><br>

      You can also make text **bold**... whoa!<br>
      Or _italic_.<br>
      Or... wait for it... **_both!_**<br>
      And feel free to go crazy ~~crossing stuff out~~.<br><br>

      There's also [links](https://www.freecodecamp.org), and<br>
      > Block Quotes!<br><br>

      And if you want to get really crazy, even tables:<br><br>

      Wild Header | Crazy Header | Another Header?<br>
      ------------ | ------------- | -------------<br>
      Your content can | be here, and it | can be here....<br>
      And here. | Okay. | I think we get it.<br><br>

      - And of course there are lists.<br>
        - Some are bulleted.<br>
          - With different indentation levels.<br>
              - That look like this.<br><br>


      1. And there are numbered lists too.<br>
      1. Use just 1s if you want!<br>
      1. And last but not least, let's not forget embedded images:<br><br>

      ![freeCodeCamp Logo](https://cdn.freecodecamp.org/testable-projects-fcc/images/fcc_secondary.svg)
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorldBis',
    data() {
        return {
      isActive: true,
      ishid: false,
    };
  },
  props: {
    msg:String,
    gethid:Function(),
    ishid1:Boolean(),
    },
  

  methods: {
    toggleClass(){
      this.isActive = !this.isActive;
      this.ishid=!this.ishid;
  },

  }
}

  


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .div{
    background-color: orange;
    width:60%;
    margin: 0 auto;
    margin-top:20px;
    display: grid;
    grid-template-columns: auto;
    padding:0;
    border-style: solid;
  }

  .div1{
    display: flex;
    flex-direction: row;
    background-color : red;
    font-size:20px;
    align-items:center;
    margin:0;
    padding:0;
    font-family: Russo One;
    border-bottom: solid;
    justify-content: space-between;
  }

  .divi{
        display: flex;
    flex-direction: row;
    align-items:center;
  }

  .div2{
    text-align : left;
    padding:10px;
    height:200px;
    overflow: auto;
    font-size:12px;
  }

    .div2bis{
    text-align : left;
    padding:10px;
    height:80vh;
    overflow: auto;
    font-size:12px;
  }

  code{color:black;
  font-family:arial;
      font-size: 12px;}

  .font{
    font-family:arial;
    font-size: 12px;
  }

  .hidden {
  display: none;
}

</style>
