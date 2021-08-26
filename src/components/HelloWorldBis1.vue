
<template>
  <div class="div" v-bind:class="ishid ? 'hidden' : ''">
    <div class="div1">
      <div class="divi">
      <div class="h3 m-1">
        <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
      </div>
      <div style="margin-left:10px">Editor</div>
      </div>
      <div class="h3 m-1">
        <button class="btn" @click="toggleClass()" v-on:click="gethid1(ishid1)"><b-icon-aspect-ratio-fill></b-icon-aspect-ratio-fill></button>
      </div>
    </div>
    <div :class="[isActive ? 'div2' : 'div2bis']">
      <h1> Welcome to my React Markdown Previewer! </h1>
      <hr class="hr1">
      <h2> This is a sub-heading... </h2>
      <hr class="hr2">
      <h3> And here's some other cool stuff: </h3>

      
      <p> Heres some code, <span class="code">{{code1}}</span>, between 2 backticks.   </p>
      <p class="code">
      {{code2}} <br><br>
      {{code3}} <br>
      {{code4}}<br>
      {{code5}}<br>
      {{code6}}<br>
      {{code7}}<br>
      </p>
      <div >
      You can also make text <b>bold</b>... whoa!<br>
      Or <i>italic.</i><br>
      Or... wait for it... <b>both!</b><br>
      And feel free to go crazy <del> crossing stuff out.</del><br><br>

      There's also <a href="default.asp" target="_blank">link</a>, and<br><br>

      <span class="vertical"></span>Block Quotes!<br><br>

      And if you want to get really crazy, even tables:<br><br>
      <table>
  <tr>
    <th><b>Wild Header</b></th>
    <th><b>Crazy Header</b></th>
    <th><b>Another Header?</b></th>
  </tr>
  <tr>
    <td>Your content can</td>
    <td>be here, and it</td>
    <td>can be here....</td>
  </tr>
  <tr>
    <td>And here.</td>
    <td>Okay.</td>
    <td>I think we get it.</td>
  </tr>
</table><br>

      <ul>
      <li>And of course there are lists.</li>
      <ul>
      <li style="list-style-type:circle;">Some are bulleted.</li>
      <ul>
              <li style="list-style-type:square;">With different indentation levels.</li>
        </ul>
        <li style="list-style-type:square;">That look like this.</li>
      </ul>
      </ul> <br>

      <ol>
  <li>And there are numbered lists too.</li>
  <li>Use just 1s if you want!</li>
  <li>And last but not least, let's not forget embedded images:</li>
  </ol>  

  <img src="https://cdn.freecodecamp.org/testable-projects-fcc/images/fcc_secondary.svg" alt="freeCodeCamp Logo">


      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorldBis1',
    data() {
        return {
      isActive: true,
      ishid1: false,
      code1: "<div></div>",
      code2: "// this is multi-line code:",
      code3:"function anotherExample(firstLine, lastLine) {",
      code4:"   {if (firstLine == '```' && lastLine == '```') {}",
      code5:"      return multiLineCode;",
      code6:"   }",
      code7:"}",

    };
  },
  props: {
    msg:String,
    gethid1:Function(),
    ishid:Boolean,
    },
  

  methods: {
    toggleClass(){
      this.isActive = !this.isActive;
      this.ishid1=!this.ishid1;
  },

  }
}

  


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .div{
    background-color:orange;
    width:70%;
    margin: 0 auto;
    margin-top:20px;
    margin-bottom:20px;
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
    height:100%;
    overflow: auto;
    font-size:12px;
  }

  code{color:black;}

  .hidden {
  display: none;
}

.hr1 {
  border-top: 2px solid black;
    background-color:black;
    opacity:100%;
}

.hr2 {
  border-top: 1px solid black;
    background-color:black;
    opacity:100%;
}

.code{
  background-color:white
}

.interline{
  line-height: 0px;
}

.vertical { 
border-left: 4px solid black; 

height: 12px; 
display: inline-block;
margin-left:20px; 
margin-right:2px; 
} 

table, td, th {
  border: 1px solid black;
}

table {
  width: 100%;
  border-collapse: collapse;
  width:auto;
}

img {
max-width:100%;
max-height:100%;
}

</style>
