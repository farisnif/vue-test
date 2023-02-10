<template>
  <div class="crd">
  <div class="container">
    <div class="header">
      <h1>A Picture of a Sunset</h1>
      <img class="image" src="https://media.cntraveler.com/photos/576834ff90b3537d7c010c05/16:9/w_2560%2Cc_limit/GettyImages-162672165.jpg" alt="A picture"/>
      <div class="subheader">
        <h2>A Picture of a Plane in a Sunset</h2>
      </div>
    </div>
  </div>
  <div class="paragraph">
    <p>This is a picture of a Boeing 787 taking off during sunset.</p>
  </div>
  <div class="buttons">
    <button class="details">Details</button>
  </div>
</div>
<button class="somethingelse" v-on:click="heading">Something Else</button>
<button class="addOne" v-on:click="duplicate">Add</button>
<button class="remove" v-on:click="takeaway">Delete One</button>
<button class="colorChanger" v-on:click="background">Color Changer</button>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })
</script>

<script>

export default {
  methods: {
    //add another card
    duplicate() {
          document.querySelector(".addOne")
      .addEventListener("click", function addCard(e) {
        const cardWhole = document.querySelector(".crd").cloneNode(true);
        document.body.appendChild(cardWhole);
      });    
    },
//change background color
    background() {
          document.querySelector(".colorChanger").addEventListener("click", function changeColor(e) {
        const div = document.querySelector("div");
        if (div.style.backgroundColor != "red") {
          div.style.backgroundColor = "red";
        } else {
          div.style.backgroundColor = "skyblue";
        }
      });
      // document.querySelectorAll(".card").forEach((item) => {
      //   if(!item.classList.contains("basic")){
      //     item.classList.add("basic");
      //     console.log(item);
      //   }
      //   else{
      //     item.classList.remove("basic");
      //     console.log(item);
      //   }
      // });
    },
//change header
    heading() {
      document.querySelector(".somethingelse")
        .addEventListener("click", function changeHeading(e) {
          document.querySelector("h1").innerHTML = "something else";
        });
      // document.querySelectorAll(".title").forEach((item) => {   
      //   if(item.innerHTML=="something else"){
      //     item.innerHTML="Chad of Cyber IST";
      //   }
      //   else{
      //     item.innerHTML="something else";
      //   }
      // });
    },

    takeaway(){
        document.querySelector(".remove")
    .addEventListener("click", function removeCard(e) {
      const cardWhole = document.querySelector(".crd").parentNode;
      cardWhole.removeChild(cardWhole.lastChild);
  });
    },

    additionalinfo(){
      document.querySelector(".details").addEventListener("click", function textVisibility(e) {
    var info = document.querySelector("p");
    if (info.style.display === "none") {
      info.style.display = "block";
    } else {
      info.style.display = "none";
    }
  });
    }

    //Kinda borked rn
    // deleter(){
    //   document.querySelector(".card:last-child").remove();
    //   console.log(card);
    // }
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
