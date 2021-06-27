<template>
<div class="flex w-full bg-gray-600">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
  </div>
</template>

<script>
export default {
    name:"Aside"
}
</script>

<style scoped>
.aside{
    display:"flex";
    width: "100%";
    height: 10vh;
}
</style>