<script setup>
import TheHeader from './TheHeader.vue';
import TheShowcase from './TheShowcase.vue';
</script>

<template>
  <div class="container">
    <header>
      <TheHeader />
    </header>

    <main class="fadeIn">
      <TheShowcase />
    </main>
    <footer>
      <br>  
      <a target="_blank" href="https://icons8.com/icon/12598/github">Icons</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
      <p>© Brendon Sadler 2023</p>
    </footer>
  </div>
</template>

<style scoped>



.container {
  display: flex;
  flex-direction: column;
  

}
header{
  width: fit-content;
}
footer{
  align-self: center;
}

.fadeIn{
  overflow: hidden;
  animation: fadeIn 2500ms ease-in forwards;
  animation-delay: 4500ms;
  opacity: 0;
}


@keyframes fadeIn {  
  from {  
      opacity:0;  
  }  

  to {  
      opacity:1;  
  }  
  
}

main{
  width: 80vw;
}
@media (max-width: 768px) {

  .container{
      width: 100%;
      height: auto;

      
  }

  header{
    align-self: center;
  }
  main{
    align-self: center;
  }



}



</style>
