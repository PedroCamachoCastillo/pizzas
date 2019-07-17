<template>
    <div>
        <div class="row">
            <div v-for="image in images" :key="image.id" class="col-md-6 col-sm-4 col-6">
                <img class="img-fluid img-galeria" v-bind:src="image.thumbnail" @click="emitImage(image)"/>
                <button class="button-galeria btn-success">Añadir Al Carrito</button>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    props: ['images'],
    methods:{
        emitImage: function(image){
            this.$emit('emitImage', image)
        }
    }
}
</script>

<style>
    .button-galeria{
        margin-bottom: 15px;
        margin-top: 15px;
        font-size: 17pt;
        margin-bottom: 25px;
        -webkit-box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        -moz-box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
    }
    .img-galeria{
        -webkit-box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        -moz-box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        margin-bottom: 15px;
        margin-top: 15px;
    }
    .img-galeria:hover{
        filter: gray;
        -webkit-filter: grayscale(1);
    }
</style>
