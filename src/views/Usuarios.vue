<template>
    <div>
        <h1>Informacion de Usuario</h1>

        <!-- <div v-for="(usuario, index) in ArregloUsuarios" :key="index">
            <router-link :to="usuario" >
                <button>{{usuario}}</button>
            </router-link>
        </div>  -->

        <router-link :to="{name:'usuarios', params: {id: Usuario}}" v-for="(Usuario, index) in ArregloUsuarios" :key="index">
            <button>{{Usuario}}</button>
        </router-link>


        <usuario/>
    </div>
</template>

<script>
import Usuario from '@/components/Usuario.vue';
export default {
    components:{
        Usuario
    },
    data(){
        return{
            ArregloUsuarios:['Jaime', 'Pandi', 'Fluffy', 'Wilson', 'Momo', 'Rafita']
        }
    }
}
</script>