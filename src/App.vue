<template>
<div id="app">
    <h2>Iron Contacts</h2>

    <td>
      <th>Picture</th>
      <th>Name</th>
      <th>Popularity</th>
    </td>    
    <table class="table" v-for="contact in myContacts">

  <tr>
    <td><img class="picture" :src="contact.pictureUrl" alt=""></td>
    <td>{{ contact.name }}</td>
    🏆
    <td>{{ contact.popularity.toFixed(2) }}</td>
  </tr>
    </table>
  
</div>
  
</template>

<script setup>
import contacts from "./contacts.json";

const myContacts = contacts;
myContacts.splice(5);
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
.table{
border: 3px;}
.picture{
  width: 20%;
}
</style>
