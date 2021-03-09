<template>
  <div class="contact-container">
    <div class="contact-info d-flex flex-column-reverse flex-sm-row text-light">
      <div class="contact-text d-flex flex-column p-4">
        <h2 class="text-center font-weight-bold">
          ¿Qué podemos hacer por ti?
        </h2>
        <h6 class="text-center pt-3">
          ¿Tienes alguna duda? ¿Quieres saber más del servicio?
          Ponte en contacto con nosotros rellenando nuestro formulario y te responderemos a la brevedad.<br>
          ¡Gracias!
        </h6>
      </div>
      <div class="div-logo py-2 px-5">
        <img class="logo" src="../assets/icons/logo.jpg" alt="logo">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact'
}
</script>

<style lang="scss" scoped>

.contact-text {
  background-color: $primary-color;
  border-top-left-radius: 80px 100px;
  border-bottom-right-radius: 80px 100px;
  justify-content: center;
  align-items: center;
  h6 {
    line-height : 25px;
  }
}

.logo {
  width: 100%;
}

</style>
