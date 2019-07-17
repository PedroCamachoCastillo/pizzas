<template>
    <div class="row">
        <div class="col-sm-8 col-12">
            <img :src="selectImage.thumbnail" class="img-fluid img-galeria-ind">
        </div>
        <div class="col-sm-4 col-12">
            <h2><strong>{{selectImage.title}}</strong></h2>
            <p>{{selectImage.details}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['selectImage']
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
    .img-galeria-ind{
        -webkit-box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        -moz-box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        box-shadow: 0px 1px 6px 1px rgba(0,0,0,2);
        margin-bottom: 15px;
        margin-top: 15px;
    }
</style>