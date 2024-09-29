<template>
    <PageLayout> 

      <template #header> 
        <h1>Info</h1> 
      </template>

      <template #default>         
        <UserInfo 
          v-for="(item, index) in users" :key="index"  :name="item.name"  :age="item.age" />         
      </template>

      <template #footer> 
        This is footer
      </template>
      
    </PageLayout>
  </template>
  
  <script setup>
  import PageLayout from './components/PageLayout.vue';
  import UserInfo from './components/UserInfo.vue';
  import { ref } from 'vue';
  

  const users = ref([
    { name: 'Oleksandr', age: 30 },
    { name: 'Victor', age: 25 },
    { name: 'Kateryna', age: 15 }
  ]);
  </script>
  