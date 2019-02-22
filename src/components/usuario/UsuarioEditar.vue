<template>
  <div class="usuario-editar">
    <h3>Usuário Editar</h3>
    <p><strong>Codigo: </strong>{{ id }}/{{ $route.params.id }}</p>
    <hr>
    <button primario @click="confirmou = true">Confirmar</button>
    <div id="rodape">
      <h3>Curso VUE</h3>
    </div>

  </div>
</template>

<script>
export default {
  props: ['id'],
  data () {
    return {
      confirmou: false,
    }
  },
  beforeRouteLeave (to, from, next) {
    if (this.confirmou) {
      next()
    }
    else {
      if (confirm('tem certeza?')) {
        next()
      }
      else {
        next(false)
      }
    }
  }
}
</script>

<style>
#rodape {
  margin-top: 1000px;
}
</style>
