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
@import url('https://fonts.googleapis.com/css?family=Lato|Merriweather|Rubik+Mono+One');

html{
  height: 100%;
}

body {
  height: 100%;
}

#app {
  height: 100%;
}

/*Menu Bar Styling*/
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #484C91;
  position: fixed;
  width: 100%;
  z-index: 500;
/*  border-radius: 25px; */
}

li {
  float: left;
  font-size: 25px;
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
  background-color: #3D3949;
  color: white;
}

a.router-link-exact-active {
  background-color: #ABE5E6;
  color: darkslategrey;
  font-weight: bold;
}

</style>
