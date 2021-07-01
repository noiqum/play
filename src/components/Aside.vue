<template>
<div class="flex w-full bg-space aside">
      <router-link to="/">
      <!-- eslint-disable-next-line vue/no-parsing-error -->
       <AsideIconBase :height="32" :width="32" >
           <Home/>
       </AsideIconBase>
       <span class="icon-name">Home</span>
      </router-link>
      <router-link to="/about">About</router-link>
  </div>
</template>

<script>
import AsideIconBase from "../components/AsideIconBase.vue";
import Home from "../assets/icon/Home.vue";
export default {
    name:"Aside",
   components:{
       AsideIconBase,
       Home
   }
}
</script>

<style lang="scss" scoped>
@import '../sass/variables.scss';
.aside{
   background-color:$purple4;
   position: fixed;
   top: 0;
   left: 0;
   min-height: 100vh;
   display: flex;
   width: 5vw;
   flex-direction: column;
   color: #006466;
   justify-content: center;
   align-items: center;
   z-index: 10;
   transition: all 0.4s ease-in-out;
   overflow: hidden;
   
   & > a {
       display: flex;
      
        & .icon-name{
            display: none;
        }
    }
    &:hover{
        width: 15vw;
         & .icon-name{
            display: flex;
        }
    }
    
    & > a:hover{
        color: aquamarine;
       
    }
}
</style>