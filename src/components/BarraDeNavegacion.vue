<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="/">{{ brand }}</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item active">
                    <a class="nav-link" href="/"><i class="fa fa-fw fa-home"></i> Inicio<span class="sr-only">(current)</span></a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link" href="/pedidos">Pedidos</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link" href="/pizzas">Todas Las Pizzas</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link" href="/about">Acerca De</a>
                </li>

                <li class="nav-item active navbar-toggler-right">
                    <a class="nav-link" href="/carrito">Carrito ({{ onCarrito }})</a>
                </li>
                <li class="nav-item active dropdown navbar-toggler-right">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Cuenta</a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                        <a class="dropdown-item" href="/login">Iniciar Sesion</a>
                        <a class="dropdown-item" href="/logout">Cerrar Sesion</a>
                    </div>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
    export default {
        data(){
            return{
                onCarrito: '0',
                brand: 'Pizzeria STELLA'
            }
        },
        created: function(){
            let datosLS = JSON.parse(localStorage.getItem('pizzas'));
            console.log(datosLS.length);
        }
    }
</script>