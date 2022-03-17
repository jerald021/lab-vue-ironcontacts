<template>
<div id="app">
  <h1>Iron Contacts</h1>
  <div class="q-pa-md q-gutter-sm">
    <q-btn color="black" @click="addContacts">Add Random Contact</q-btn>
    <q-btn color="black" @click="sortByPopularity">Sort by Popularity</q-btn>
    <q-btn color="black" @click="sortByName">Sort by name</q-btn>
  </div>


  <table>
    <tr>
      <th>Picture</th>
      <th>Name</th>
      <th>Popularity</th>
      <th>Won Oscar</th>
      <th>Won Emmy</th>
    </tr>        
    <tr v-for="contact in myContacts.slice(0,5)" :key="contact.id">
      <td><q-img  spinner-color="white" style="height: auto; width: 100px" class="picture shadow-15" :src="contact.pictureUrl" alt=""/></td>      
      <td>{{ contact.name }}</td>    
      <td>{{ contact.popularity.toFixed(2) }}</td>
      <td v-if="contact.wonOscar">🏆</td>
      <td v-else></td>
      <td v-if="contact.wonEmmy">🏆</td>
      <td v-else> </td>
    </tr>    
  </table>
  
</div>  
</template>

<script setup>
//IMPORTS
import contacts from "./contacts.json";

//VARS
const myContacts = contacts;
const isRepeated = false;
// myContacts.splice(5);

//FUNCTIONS
function addContacts(){

}
function sortByName(){

}
function sortByPopularity(){

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
