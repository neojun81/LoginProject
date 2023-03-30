<template>
  <div>
    <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <header class="header">
      <nav class="navbar">
        <router-link class="a" to="/">Home</router-link>
        <router-link class="a" to="/">About</router-link>
        <router-link class="a" to="/">Services</router-link>
        <router-link class="a" to="/">Contact</router-link>
      </nav>
      <from action="#" class="search-bar">
        <input text="text" placeholder="Search...">
        <button type="submit"><magnify class="i"/></button>
      </from>
    </header>
    <div class="background"></div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
body {
  background: #020410;
}
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 25px 12.5%;
  background: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 100;
}
.navbar .a {
  position: relative;
  font-size: 16px;
  color: #00cccc;
  text-decoration: none;
  font-weight: 500;
  margin-left: 30px;
}
.navbar .a::after{
  content: '';
  position: absolute;
  left: 0;
  bottom: -6px;
  width: 100%;
  height: 2px;
  background: #00cccc;
  border-radius: 5px;
  transform: translateY(10px);
  opacity: 0;
  transition: .5s;
}
.navbar .a:hover:after{
  transform: translateY(0);
  opacity: 1;
}
.search-bar {
  width: 250px;
  height: 45px;
  background: transparent;
  border: 2px solid #00cccc;
  border-radius: 6px;
  display: flex;
  align-items: center;
 }
 .search-bar input {
  width: 100%;
  background: transparent;
  border: none;
  outline: none;
  font-size: 16px;
  color: #00cccc;
  padding-left: 10px;
 }
 .search-bar input::placeholder {
  color:#00cccc
 }
 .search-bar button{
  width: 40px;
  height: 100%;
  background: transparent;
  display: flex;
  border: none;
  outline: none;
  justify-content: center;
  justify-items: center;
  cursor: pointer;
  align-items: center;
 }
 .search-bar button .i{
  font-size: 22px;
  color: #00cccc;
 }
 .background {
  width: 100%;
  height: 100vh;
  background: url('./assets/back.jpg') no-repeat;
  background-size: cover;
  background-position: center;
  filter: blur(10px)
}
</style>
