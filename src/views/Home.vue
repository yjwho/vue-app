<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Fighting Sneaky Racism" />
    
    <Issue name = "Jackie" issue="I called Alex white."/>
    <Issue name = "Jackie" issue="Alex is white."/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

//need to import a vue
import Issue from "@/components/story.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    Issue
  }
};
</script>
