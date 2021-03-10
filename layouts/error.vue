<template>
  <div class="error-container text-center">
    <h2 class="py-5">
      Uups...!
    </h2>
    <h1 v-if="error.statusCode === 404" class="mb-6">
      No hemos encontrado la página que has solicitado. <br>
      😱
    </h1>
    <h1 v-else>
      Uups, ha ocurrido un error! <br>
      😱
    </h1>
    <NuxtLink to="/">
      <h4 class="py-5">
        Volver al inicio
      </h4>
    </NuxtLink>
  </div>
</template>

<script>
export default {
  layout: 'blog',
  props: ['error']
}
</script>

<style lang="scss" scoped>

.error-container {
  color: $secondary-color;
}

</style>
