<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      A paragraph here.
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
@import url('https://fonts.googleapis.com/css?family=Lato|Merriweather|Rubik+Mono+One');
html {
  height: 100%;
}
body {
  text-align: center;
  
  background: linear-gradient(45deg,#ABE5E6,#7062F0);
  /*linear-gradient(to bottom right, #fccdd3, #c9a8bc, #9386a0, #5e677e, #2f4858);*/
  background-size: cover;
}




/*
* default HelloWorld component styling

h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
*/
</style>
