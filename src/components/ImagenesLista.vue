<template>
    <div>
        <div class="row">
            <div v-for="image in images" :key="image.id" class="col-md-6 col-sm-4 col-6">
                <img class="img-fluid img-galeria" v-bind:src="image.url" @click="emitImage(image)"/>
                <button class="button-galeria btn-success" id="navbarDropdownMenuLink" data-toggle="dropdown">Añadir Al Carrito</button>
                <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                    <a class="dropdown-item" href="#" @click="addCarrito(image, 'personal')">Personal</a>
                    <a class="dropdown-item" href="#" @click="addCarrito(image, 'mediana')">Mediana</a>
                    <a class="dropdown-item" href="#" @click="addCarrito(image, 'grande')">Grande</a>
                    <a class="dropdown-item" href="#" @click="addCarrito(image, 'familiar')">Familiar</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
pizzasCarrito: [];
export default {
    props: ['images'],
    methods:{
        emitImage: function(image){
            this.$emit('emitImage', image);
        },
        addCarrito: function(image, tamano){
            this.pizzasCarrito = JSON.parse(localStorage.getItem('pizzas'));
            console.log(this.pizzasCarrito);
            if(this.pizzasCarrito != null){
                console.log("No NULL");
                this.pizzasCarrito.push({
                    nombre: image.nombre,
                    precioBase: tamano,
                    detalles: image.detalles,
                    url: image.url,
                });
            }else{
                console.log("NULL")
                this.pizzasCarrito = ({
                    nombre: image.nombre,
                    precioBase: tamano,
                    detalles: image.detalles,
                    url: image.url,
                });
            }
            localStorage.setItem('pizzas', JSON.stringify(this.pizzasCarrito));
        }
    }
}
</script>

<style>
    .button-galeria{
        margin-bottom: 15px;
        margin-top: 15px;
        margin-left: 15px;
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
