<template>
    <div class="galeria container mt-4">
        <img alt="Pizzeria Chaira" src="../assets/logoPizzeriaLit.png">
        <ImagenIndividual :selectImage="selectImage"></ImagenIndividual>
        <div class=".label-galeria-anuncio badge-danger">MENÚ DE PIZZAS</div>
        <ImagenesLista v-bind:images="images" v-on:emitImage="showImage"></ImagenesLista>
    </div>
</template>

<script>
import ImagenIndividual from '@/components/ImagenIndividual.vue';
import ImagenesLista from '@/components/ImagenesLista.vue';

export default {
    name: 'pizzas',
    components: {ImagenIndividual, ImagenesLista},
    data () {
        return {
            selectImage: '',
            images: [
                {id: 1, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto01b.png'},
                {id: 2, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto02b.png'},
                {id: 3, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto02b.png'},
                {id: 4, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto02b.png'},
                {id: 5, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto02b.png'},
                {id: 6, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto02b.png'},
                {id: 7, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto02b.png'},
                {id: 8, title: 'Pizza Nueva', details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets', thumbnail: 'https://videotutoriales.com/egipto02b.png'}

            ]
        }
    },
    methods:{
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
