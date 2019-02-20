<template>
  <div id="app">
    
      <ul>
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/issues">Issues</router-link>
        </li>
        <li>
            <router-link to="/about">About</router-link>
        </li>
      </ul>
  
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
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

/*Menu Bar Styling*/
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
/*  border-radius: 25px; */
}

li {
  float: left;
  font-size: 20px;
  font-family: 'Lato', sans-serif;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change the link color to #111 (black) on hover */
li a:hover {
  background-color: #000780;
  color: white;
}

a.router-link-exact-active {
  background-color: #ABE5E6;
  color: darkslategrey;
  font-weight: bold;
}

/* Button Styling */
.button {
  font-family: 'Lato', sans-serif;
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 16px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 25px;
  margin: 4px 2px;
  -webkit-transition-duration: 0.4s; /* Safari */
  transition-duration: 0.4s;
  cursor: pointer;
}

.button1 {
  background-color: #F05E80; 
  border: 2px solid #F05E80;
}

.button1:hover {
  background-color: white;
  color: #F05E80;
}

</style>
