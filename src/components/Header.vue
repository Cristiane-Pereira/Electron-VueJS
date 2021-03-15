<template>

 <header>
   <nav class="container">
      <a href="/"><img id="logo" src="../assets/unnamed.png" alt="logo"></a>
    
      <p id="menu-button"><i class='bx bx-menu'></i></p>
   
   </nav>
 </header>

</template>



<script>

export default {
  name: 'Header'
}
</script>



<style scoped>

nav{
  display: flex;
  justify-content: space-between;
}

header{
   background-color: var(--color-background-nav);
   height:60px;
   width:100%;
   display:flex;
   justify-content: center;
   align-items: center;


}

#logo {
  width:47px;
 
}

#menu-button {
   color:#ffffff;
   font-size:35px;
   cursor: pointer;
  
}

</style>