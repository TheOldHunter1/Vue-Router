<template>
    <div class="container">
        <div class="cover">
            <div class="col-md-12">
                <h3>Productos</h3>
            </div>
            <div class="row" >
                <div class="col-md-3" v-for="producto in productos" :key="producto.id">
                    <div class="col-md-12">
                        <img src="http://placehold.it/200x100/000">
                    </div>
                    <div class="col-md-12">
                        <h4>{{producto.titulo}}</h4>
                        <p>{{producto.desc}}</p>
                        <router-link class="btn btn-info btn-sm" :to="{name:'producto', params:{id:producto.id}}"> Ver detalle </router-link> <br>  <br>
                        <a href="#" class="btn btn-success btn-sm">Agregar al carro</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            productos:[
                {id:1,titulo:'pc low cost', desc:'Pc gama baja'},
                {id:2,titulo:'pc medium cost', desc:'Pc gama media'},
                {id:3,titulo:'pc high cost', desc:'Pc gama alta'},
                {id:4,titulo:'pc supreme cost', desc:'Pc gama gamer'},
            ]
        }
    }
}
</script>

<style>
    .cover{
        padding: 20px;
        margin: 40px 2px;
        border: 1px solid #D2E0E6; 
    }
</style>