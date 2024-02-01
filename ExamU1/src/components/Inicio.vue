<template>
  <div class="px-3 py-2">
    <b-nav-item>
      <b-link :to="{name: 'inicio'}">
        Inicio
      </b-link>
    </b-nav-item>
    <b-nav-item>
      <b-link :to="{name: 'formulario'}">
        Formulario
      </b-link>
    </b-nav-item>
    <b-nav-item>
      <b-link :to="{name: 'paginacion'}">
        Paginacion
      </b-link>
    </b-nav-item>
  </div>
</template>


<script>
 export default {
    data() {
      return {
        items: [
          {
            text: 'Inicio',
            href: '#',
            to:"formulario"
          },
          {
            text: 'Formulario',
            href: '#',
            to: "paginacion"
          },
          {
            text: 'Paginacion',
            href: '#',
            to: "inicio"
          },
        ]
      }
    }
  }
</script>
<style>

</style>