<template>
  <div class="home">
    <HelloWorld msg="Fighting Sneaky Racism" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>

<style>
body {
  text-align: center;
  background: linear-gradient(45deg,#ABE5E6,#7062F0);
  /*linear-gradient(to bottom right, #fccdd3, #c9a8bc, #9386a0, #5e677e, #2f4858);*/
  background-size: cover;
}

h1, h2 {
  display: inline-block;
  color: #FFFFFF
}
h1 {
  font-size: 80px;
  font-family: 'Rubik Mono One', sans-serif;
}
h2 {
  font-size: 20px;
  font-family: 'Merriweather', sans-serif;
}
</style>
