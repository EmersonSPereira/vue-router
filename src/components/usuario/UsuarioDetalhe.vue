<template>
    <div class="usuario-detalhe">
        <h3>Usuário Detalhe</h3>
        <p><strong>Codigo: </strong>{{ id }}</p>
        <!-- :to="`/usuario/${id}/editar`" -->
        <router-link tag="Button" primario  :to="{ name: 'editarUsuario', params:{id: $route.params.id},
        hash:'#rodape'} ">
        Editar
        </router-link>
    </div>
</template>

<script>
export default {
    props: ['id'],
    beforeRouteEnter (to, from, next) {
        // console.log('dentro do componente  -> usuário deltalhe')
        next()
    }
    // data(){
    //     return {
    //         id: this.$route.params.id
    //     }
    // },
    // watch:{
    //     $route(to /* ,from*/){
    //         this.id = to.params.id
    //     }
    // },

}
</script>

<style>

</style>
