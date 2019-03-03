<template>
  <div class="hello">
    <br>
    <br>
    <br>
    <br>
    <br>
    <h1>{{ msg }}</h1>
    <br>
    <br>
    <br>

    <h2>
      Read about others' experiences with racism and microaggressions <b>on campus</b> and record your own!
    </h2>

    <br>
    <br>
    <br>
<router-link to="/issues" tag="submit">
    <button class="button1" >VIEW OTHERS' STORIES</button>
  </router-link>
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
<style scoped>
html {
  height: 100%;
}
#hello{
  height: 100%;
  margin-top: 40px;
}

h1, h2 {
  display: inline-block;
  color: #FFFFFF
}
h1 {
  font-size: 100px;
  font-family: 'Rubik Mono One', sans-serif;
}
h2 {
  font-size: 30px;
  font-family: 'Lato', sans-serif;
}

h4 {
  font-weight: bolder;
}
/* Button Styling */

.button1 {
  background-color: transparent; 
  border: 2px solid white;
  color: white;
  font-size: 30px;
  font-weight: bold;
  padding: 10px;
  text-align: center;
  text-decoration: none;
  -webkit-transition-duration: 0.4s;
  transition-duration: 0.4s;
  cursor: pointer;
}

.button1:hover {
  background-color: white;
  color: #7062F0;
}


</style>
