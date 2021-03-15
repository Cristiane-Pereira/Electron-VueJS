<template>

 <main>

  <div class="text-top">Fotos / Imagens</div>
  <table class="img">
     <tr v-for="item in list" v-bind:key="item.id">
        <td>{{item.url}}</td>
      </tr>
  </table>
 
 </main>

</template>


<script>
import api from '@/services/api.js';

export default {
  name: 'Main',
  data() {
    return {list:undefined}
  },
  mounted() {
    api.get('//picsum.photos/v2/list')
    .then(response => {
      this.list = response.data;
      console.log(response.data);
    })
  }
}
</script>

<style scoped>

main {
   background-color: var(--color-background-home);
   
}

.text-top{
    text-align: center;
    color: var( --color-text-light);
    font-size: 25px;
    padding-top: 3rem;
}

.img {
    display:colums;
    justify-content: center;
    align-items: center;
}

</style>