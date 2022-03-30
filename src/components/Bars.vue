<template>
<div class="wrapper" id="resultBar">
  <left>
    <h2>Results:</h2>
    <br/>
    <div v-for="(item, key) in data" v-bind:key="key">
      <span>
        <h4>Answer "{{key}}":</h4>
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        {{item}} vote(s)
        <br/><br/>
      </span>
    </div>
 </left>

  <right>
    <div class="bar" v-for="(item, key) in data" v-bind:key="key">
      {{key}}
      <div v-bind:style="{width: item + 'em'}">
        <div> <br/> </div>
        <span class="answerBar"> {{item}} </span>
      </div>
    </div>

  </right>


</div>
</template>

<script>
//import io from 'socket.io-client';
//const socket = io();

export default {
  name: 'Bars',
  props: {
    data: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



/*.bar {
  display: flex;
  height: 3em;
  alignment: left;
  margin: 1em 0 1em 0;
}

.bar .answerBar {
  position: relative;
  color: white;
}

.bar:nth-child(1) div:nth-child(1), #barNo0 {
  background-color: #1A237E;
  border-radius: 0 0.5em 0.5em 0;
  margin-left: 1em;
}
.bar:nth-child(2) div:nth-child(1), #barNo1 {
  background-color: #1565C0;
  border-radius: 0 0.5em 0.5em 0;
  margin-left: 1em;
}
.bar:nth-child(3) div:nth-child(1), #barNo02 {
  background-color: #0288D1;
  border-radius: 0 0.5em 0.5em 0;
  margin-left: 1em;
}
.bar:nth-child(4) div:nth-child(1), #barNo3 {
  background-color: #00ACC1;
  border-radius: 0 0.5em 0.5em 0;
  margin-left: 1em;
}
.bar:nth-child(5) div:nth-child(1), #barNo4 {
  background-color: #009688;
  border-radius: 0 0.5em 0.5em 0;
  margin-left: 1em;
}
.bar:nth-child(6) div:nth-child(1), #barNo5 {
  background-color: #66BB6A;
  border-radius: 0 0.5em 0.5em 0;
  margin-left: 1em;
}

#resultBar {
  display: grid;
  grid-template: "left right";
  grid-template-columns: 1fr 3fr;
  padding: 2em 1em 2em 1em;

}

#resultBar > left {
  grid-area: left;
  display: block;
  margin: auto auto auto 10px;
}

#resultBar > right {
  grid-area: right;
  background-color: #fffffe;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.06), 0 10px 20px rgba(0, 0, 0, 0.12);
  margin: auto 20px auto 20px;
  padding: 20px 40px 20px 60px;
  border: solid 3px #03b6ff;
  border-radius: 30px;
}*/

</style>
