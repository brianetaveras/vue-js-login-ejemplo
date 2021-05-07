<template>
    <div class="comentario">
        <img :src="info.pic" alt="" class="foto-de-perfil">
        <div class="nombre-de-usuario">{{info.username}}</div>
        <p class="contenido">{{info.comentario}}</p>
        <div class="fecha">{{info.fecha}}</div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
    props: {
        info: {
            type: Object,
            required: true,
        }
    }
})
</script>

<style lang="scss" scoped>
.comentario {
    display: grid;
    grid-template-areas: "pic name"
                         "pic content"
                         "fecha fecha";
    grid-template-columns: 10% 90%;
    grid-template-rows: 40px auto 20px ;
    width: 100%;
    background: rgba(255, 255, 255, 0.4);
    border-radius: 10px;
    padding: 10px;
    box-sizing: border-box;
    margin: 10px 0;

    .foto-de-perfil {
        grid-area: pic;
        width: 40px;
        height: 40px;
        object-fit: cover;
        border-radius: 50%;
    }

    .nombre-de-usuario {
        grid-area: name;
    }

    .contenido {
        grid-area: content;
        margin: 0;
    }

    .fecha {
        grid-area: fecha;
        text-align: right;
    }
}
</style>