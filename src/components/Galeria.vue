<template>
    <div class="galeria container mt-4">
        <ImagenIndividual :selectImage="selectImage"></ImagenIndividual>
        <div class=".label-galeria-anuncio badge-danger">LO NUEVO</div>
        <ImagenesLista v-bind:images="images" v-on:emitImage="showImage"></ImagenesLista>
    </div>
</template>

<script>
import ImagenIndividual from './ImagenIndividual.vue';
import ImagenesLista from './ImagenesLista.vue';
import axios from 'axios';

export default {
    name: 'galeria',
    components: {ImagenIndividual, ImagenesLista},
    data () {
        return {
            pizzasRecientes: null,
            selectImage: '',
            images: [
                {id: 1, nombre: 'Pizza Nueva', detalles: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', url: 'https://videotutoriales.com/egipto01b.png'},
                {id: 2, nombre: 'Pizza Nueva', detalles: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', url: 'https://videotutoriales.com/egipto02b.png'}
            ]
        }
    },
    mounted(){
        this.getPizzasRecientes();
    },
    methods:{
        getPizzasRecientes(){
            axios
                .get('https://xxx.xxx.com/xxxx')
                    .then( response=>{
                        this.pizzasRecientes = response.data
                    })
                    .catch( e=> console.log(e))
        },
        showImage: function(image){
            this.selectImage = image
        }
    }
}
</script>

<style>
    .label-galeria-anuncio{
        height: 40px;
        font-size: 30pt;
        margin-bottom: 30px;
    }
</style>
