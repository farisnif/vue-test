<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 + Vite" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
.crd{
  padding: 12px;
  background-color: skyblue;
  border-radius: 12px;
  border: 6px solid black;
  max-width: 300px;
  padding: 12px;
  float: left;
}
.image{
  width: 100%;
}
h1{
  font-size: 30px;
  text-align: center;
}
h2{
  font-size: 18px;
  text-align: center;
}
.buttons{
  margin: 0;
  text-align: center;
  display: none;
  clear: both;
}
p{
  text-align: center;
  display: none;
}
@media (min-width: 500px) and (max-width: 800px) {
  .buttons {
    display: block;
    margin: 0 auto;
    text-align: center;
  }
}
.somethingelse {
  font-size: 18px;
  display: block;
  margin: 0;
}
.somethingelse:hover{
  background-color: orange;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
.somethingelse:focus{
  background-color: orange;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
.addOne{
  font-size: 18px;
  display: block;
  margin: 0;
}
.addOne:hover{
  background-color: lightseagreen;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
.addOne:focus{
  background-color: lightseagreen;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
.remove {
  font-size: 18px;
  display: block;
  margin: 0;
}
.remove:hover {
  background-color: green;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
.remove:focus{
  background-color: green;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
.colorChanger{
  font-size: 18px;
  display: block;
  margin: 0;
}
.colorChanger:hover{
  background: linear-gradient(
    to right,
    red,
    yellow,
    red,
    blue,
    cyan,
    blue,
    violet
  );
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
.colorChanger:focus{
  background: linear-gradient(
    to right,
    red,
    yellow,
    red,
    blue,
    cyan,
    blue,
    violet
  );
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}
@media (max-width: 500px) {
  .crd {
    transform: scale(0.8);
  }
  .image {
    width: 300px;
  }
  h1 {
    font-size: 18px;
  }
  p {
    font-size: 12px;
  }
};
</style>
