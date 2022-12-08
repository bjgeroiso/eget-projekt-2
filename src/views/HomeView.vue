<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

// function helloWorld () {

  let items = [{name: "ASUS Xonar AE 7.1", image: "https://cdn.inet.se/product/688x386/6302211_5.png", price: 890, url: "https://www.inet.se/produkt/6302211/asus-xonar-ae-7-1" ,class: "item1"}, 
                   {name: "Arctic Cooling MX-6 2g", image: "https://cdn.inet.se/product/688x386/5324189_0.png", price: 79, url: "https://www.inet.se/produkt/5324189/arctic-cooling-mx-6-2g", class: "item2"},
                   {name: "Alphacool D-RAM Module", image: "https://cdn.inet.se/product/688x386/6911971_4.png", price: 449, url: "https://www.inet.se/produkt/6911971/alphacool-d-ram-module-till-d-ram-cooler", class: "item3"},
                   {name: "Arctic Freezer i35 ARGB", image: "https://cdn.inet.se/product/688x386/5323688_8.png", price: 449, url: "https://www.inet.se/produkt/5323688/arctic-freezer-i35-argb", class: "item4"},
                   {name: "Logitech G903 Hero Wireless", image: "https://cdn.inet.se/product/688x386/6600940_22.png", price: 599, url: "https://www.inet.se/produkt/6600940/logitech-g903-hero-wireless", class: "item5"},
                   {name: "Taurus GM1-W", image: "https://cdn.inet.se/product/688x386/6608767_6.png", price: 199, url: "https://www.inet.se/produkt/6608767/taurus-gm1-w", class: "item6"}] as const;
  let categories = [{name: "kylare och kylpasta", number: "3"},
                   {name: "datormöss", number: "2"}, 
                   {name: "moderkort", number: "1"}, 
                   {name: "se annat", number: "..."}] as const;

  // return {items, categories};
// }

// helloWorld();

// export default {
//     setup () {
    // const items = [{name: "ASUS Xonar AE 7.1", image: "https://cdn.inet.se/product/688x386/6302211_5.png", price: 890, url: "https://www.inet.se/produkt/6302211/asus-xonar-ae-7-1" ,class: "item1"}, 
    //                {name: "Arctic Cooling MX-6 2g", image: "https://cdn.inet.se/product/688x386/5324189_0.png", price: 79, url: "https://www.inet.se/produkt/5324189/arctic-cooling-mx-6-2g", class: "item2"},
    //                {name: "Alphacool D-RAM Module", image: "https://cdn.inet.se/product/688x386/6911971_4.png", price: 449, url: "https://www.inet.se/produkt/6911971/alphacool-d-ram-module-till-d-ram-cooler", class: "item3"},
    //                {name: "Arctic Freezer i35 ARGB", image: "https://cdn.inet.se/product/688x386/5323688_8.png", price: 449, url: "https://www.inet.se/produkt/5323688/arctic-freezer-i35-argb", class: "item4"},
    //                {name: "Logitech G903 Hero Wireless", image: "https://cdn.inet.se/product/688x386/6600940_22.png", price: 599, url: "https://www.inet.se/produkt/6600940/logitech-g903-hero-wireless", class: "item5"},
    //                {name: "Taurus GM1-W", image: "https://cdn.inet.se/product/688x386/6608767_6.png", price: 199, url: "https://www.inet.se/produkt/6608767/taurus-gm1-w", class: "item6"}];

    // const categories = [{name: "kylare och kylpasta", number: "3"}, 
    //                     {name: "datormöss", number: "2"}, 
    //                     {name: "moderkort", number: "1"}, 
    //                     {name: "se annat", number: "..."}, ]

    // return { items, categories }
    // }
// }
</script>

<template>
    <!-- <div class="test"> -->
      <div class="kategori-del">
        <input class="kategorier" type="text" placeholder="sökord ...">
        <a href="https://google.com" class="knapp" value="sök"><p>sök</p></a> 
        <div class="kategorilista">
          <br>
          <h2>&nbsp;valda kategorier:</h2>
          <div class="lista">
            <p v-for="i in 4">
              <p>&nbsp; {{categories[i-1].name}}, {{categories[i-1].number}}</p>
            </p>
          </div>
        </div>  
      </div> 
        <!-- <input type="text" placeholder="sök ..."> -->
      <!-- </div> -->
      <div class="produkter">
        <div style="display: flex; width: 1000px;">
          <a :href="items[index-1].url" target="_blank" :class="[items[index-1].class]" v-for="index in 6">
            <div class="namn">{{ items[index-1].name }}</div>
            <div class="pris">{{ items[index-1].price }}kr</div>
            <div class="bild">
              <img :src="items[index-1].image"/>
            </div>
          </a>
        </div>
      </div>
    <!-- </div> -->
</template>

<style lang="scss">

  .kategori-del {
    position: absolute;
    top: 10vh;
  }

  .namn {
    text-align: center;
    width: 17vw;
    height: 30px;
    top: 0;
    background-color: rgb(150, 150, 150);
    color: black;
    position: absolute;
  }

  .bild {
    top: 30px;
    width: 17vw;
    height: 150px;
    background-color: rgb(100, 100, 100);
    position: absolute;
    overflow: hidden;
    display: flex;
    justify-content: center;
  }

  .bild img {
    width: auto;
    height: 150px;
    // width: 100%;
  }

  .pris {
    width: 17vw;
    text-align: center;
    height: 20px;
    top: calc(200px - 20px);
    background-color: rgb(150, 150, 150);
    color: black;
    position: absolute;
  }

  .item1 {
    width: 17vw;
    height: 200px;
    top: 15vh;
    left: calc(42.5vw - 8.5vw);
    position: absolute;
    // display: flex;
    // justify-content: center;
  }

  .item2 {
    width: 17vw;
    height: 200px;
    top: 15vh;
    left: calc(85vw - 17vw - 8.5vw);
    position: absolute;
  }

  .item3 {
    width: 17vw;
    height: 200px;
    top: 15vh;
    left: 8.5vw;
    position: absolute;
  }

  .item4 {
    width: 17vw;
    height: 200px;
    top: calc(15vh + 250px);
    left: calc(42.5vw - 8.5vw);
    position: absolute;
  }

  .item5 {
    width: 17vw;
    height: 200px;
    top: calc(15vh + 250px);
    left: 8.5vw;
    position: absolute;
  }

  .item6 {
    width: 17vw;
    height: 200px;
    top: calc(15vh + 250px);
    left: calc(85vw - 17vw - 8.5vw);
    position: absolute;
  }

  .produkter {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 85vw;
    height: 90vh;
    background-color: rgb(41, 41, 41);
    display: flex;
  }

  .kategorier {
    position: absolute;
    top: 0;
    left: 0;
    width: 11vw;
    height: 5vh;
    background-color: rgb(230,230,230);
    border: 0;
    color: black;
  }

  .knapp {
    line-height: 5vh;
    position: absolute;
    top: 0;
    left: 11vw;
    width: 4vw;
    height: 5vh;
    background-color: rgb(130,130,130);
    color: white;
    border: 0;
    text-align: center;
    text-justify: auto;
  }

  .kategorilista {
    position: absolute;
    top: 5vh;
    left: 0;
    background-color: rgb(180,180,180);
    color: black;
    width: 15vw;
    height: 85vh;
    // display: flex;
    // flex-direction: column;
    // flex-wrap: wrap;
    // align-items:;
  }

  .lista {
    position: absolute;
    top: 10vh;
    // background-color: rgb(180,180,180);
    display: flex;
    flex-direction: column;
  }

  .lista p {
    width: 15vw;
    margin-top: 5px;
    // background-color: aqua;
  }

  .knapp:hover {
    background-color: rgb(60,60,60);
  } 

  .knapp.p {
    padding: 0;
  }

  .test {
    top: 10vh;
    position: absolute;
    width: 100%;
    height: 100vh;
  }

</style>