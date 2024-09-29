<script setup>
    import defineProps from 'vue';
    defineProps(['name', 'age']);
</script>

<template>
    <div class="UserInfo">
        <div class="user-card">
        <p>   Name: {{ name }}</p>
        <p v-if="age < 18 ">  Not Allowed</p>  
        <p v-else>   Age: {{ age }}</p>       
    </div>
    </div>
</template>

<style>
.UserInfo {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-content: space-between;
}
.user-card{
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px solid black;
    border-radius: 8px;
    padding: 20px;
    margin: 10px 0;
}
</style>