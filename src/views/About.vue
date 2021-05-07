<template>
  <div class="about">
  <Comentario :key="index" v-for="(comentario, index) in comentarios" :info="comentario"/>
  </div>
</template>


<script>

import Vue from 'vue';
import Comentario from '@/components/Comentario';
export default Vue.extend({
  components: {
    Comentario
  },
  data(){ 
    return {
      comentarios: [
        {
          username: 'MrHatBirb',
          pic: "https://images.unsplash.com/photo-1522926193341-e9ffd686c60f",
          comentario: "Hola me llamo gojan con j",
          fecha: "Viernes 13"
        },
        {
          username: 'MrHatBirb',
          pic: "https://images.unsplash.com/photo-1522926193341-e9ffd686c60f",
          comentario: "Emmy va a la clase, que chevere!",
          fecha: "Viernes 14"
        },
        {
          username: 'MrHatBirb',
          pic: "https://images.unsplash.com/photo-1522926193341-e9ffd686c60f",
          comentario: "Ps yo creo que la original es mejor >:(",
          fecha: "Viernes 15"
        },
      ]
    }
  }

});
</script>

<style lang="scss" scoped>
.about {
  max-width: 600px;
  margin: 10px auto;
}
</style>