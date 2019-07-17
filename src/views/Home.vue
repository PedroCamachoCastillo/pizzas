<template>
  <div class="home">
    <img alt="Pizzeria Chaira" src="../assets/logoPizzeria.png">
    <Galeria/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Galeria from '@/components/Galeria.vue';

  export default{
    name: 'app',
    components:{
      Galeria
    }
  }
</script>
