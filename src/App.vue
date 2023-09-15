<script setup>
import HelloWorld from './components/HelloWorld.vue'
import CardFood from './components/CardFood.vue';


</script>

<template>
  <div class="container">
    <div class="container-form">
      <v-card class="c-f">
        <div class="title" >
          <v-icon 
          size="48"
          color="#8338ec"
          icon="mdi-silverware-clean"></v-icon>
          <h1 class="text-title">
          FoodApp
          </h1>
        </div>
        
        <form>
        <v-text-field  
        variant="outlined" 
        label="Name"
        prepend-icon="mdi-rename"
        ></v-text-field>
        <v-combobox
        variant="outlined"
        prepend-icon="mdi-food-takeout-box"
        label="Food Category"
        :items="['Mexican food','Italian food','Thai food','Korean food','Japanese Food','American Food']"
        ></v-combobox>
        <v-textarea 
        variant="outlined"
        label="recipe"
        prepend-icon="mdi-book-open-outline"
        ></v-textarea>

          <v-btn 
          type="submit"
          class="btn-submit"
          prepend-icon="mdi-plus"
          variant="tonal"
          >Add</v-btn>
      </form>
      </v-card>
    </div>
    <div class="container-cards">
      <CardFood title="Tacos al pastor" 
      culinary-category="Mexican Food"
      recipe="Tortilla de maíz rellena con carne de cerdo condimentada con una salsa de especias y chiles secos."
      image="../src/assets/mexican-food.jpg"></CardFood>

      <CardFood title="Ramen clasico" 
      culinary-category="Japanese Food"
      recipe="Consiste en una sopa hecha con caldo de carne o verduras y salsa de soja al que se añaden unos fideos largos de harina de trigo y otros ingredientes, como huevo, carne o verduras."
      image="../src/assets/japanese-food.jpg"></CardFood>

      <CardFood title="Pizza italiana" 
      culinary-category="Italian Food"
      recipe="Pan plano horneado, habitualmente de forma redonda, elaborado con harina de trigo, sal, agua y levadura, cubierto con salsa de tomate y queso. Preparar pizza pero no agregar pinia ni catpsu"
      image="../src/assets/italian-food.jpg"></CardFood>

      <CardFood title="Pad Thai" 
      culinary-category="Thai Food"
      recipe="Tallarines de arroz salteados con pollo, gambas o tofu y condimentado con salsa de pescado, salsa de soja, huevo, lima, chile y azúcar"
      image="../src/assets/thai-food.jpg"></CardFood>

      <CardFood title=" Bibimbap" 
      culinary-category="Korean Food"
      recipe="Consiste en un cuenco de arroz con vegetales y carne encima"
      image="../src/assets/korean-food.jpg"></CardFood>


      <CardFood title="Chicago Style Pizza" 
      culinary-category="American Food"
      recipe="La auténtica pizza estilo Chicago tiene una base de pan gruesa, honda y crujiente, rellena de queso y salsa de tomate en trozos."
      image="../src/assets/american-food.jpg"></CardFood>
    </div>
  

   
  </div>
</template>

<style scoped>


@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:ital,wght@1,500&family=Roboto:ital,wght@0,500;1,400&display=swap');

.container{
  width: 100%; /* Ancho del viewport */
  height: 100vh; /* Alto del viewport */
  display: flex;
  flex-direction: row;
  background-color: #2a282a;
}

.container-form{
  width: 40%;
}

.container-cards{
  display: flex;
  flex-wrap: wrap;
  width: 60%;
  overflow: auto;
}

.cssbody{
  background-color: #2a282a;
}

.c-f{
  min-width: 250px;
  max-width: 450px;
  margin: auto;
  padding: 15px;
  margin-top: 10px;
}

text-title{
 font-size: 50px;
}

.title{
  display: flex;
  flex-direction: row;
  gap: 2px;
  margin-bottom: 10px;
}

.btn-submit{
  color: #3a86ff ;
  margin-left: 43px;
}

</style>
