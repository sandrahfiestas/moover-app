<template>
  <div class="container">
    <h1 v-if="error.statusCode === 404">
      No hemos encontrado la página que has solicitado.
    </h1>
    <h1 v-else>
      Oops, ha ocurrido un error
    </h1>
    <NuxtLink to="/">
      Volver al inicio
    </NuxtLink>
  </div>
</template>

<script>
export default {
  layout: 'blog',
  props: ['error'] // Aquí puedes configurar un layout customizado para la página de error
}
</script>
