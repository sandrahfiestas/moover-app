<template>
  <div class="container">
    <h1 class="py-5 text-center">
      ¿Qué deseas hacer?
    </h1>

    <div class="row">
      <div class="col-md-4 col-xl-3">
        <div class="card bg-c-primary order-card">
          <nuxt-link to="/tracking">
            <div class="card-block">
              <h5 class="m-b-20 text-center">
                <p>Rastrear Envío</p>
                <img src="../assets/icons/ruta.png" alt="Facebook">
              </h5>
            </div>
          </nuxt-link>
        </div>
      </div>
      <div class="col-md-4 col-xl-3">
        <div class="card bg-c-primary order-card">
          <nuxt-link to="/registerOrder">
            <div class="card-block">
              <h5 class="m-b-20 text-center">
                <p>Cotizar y Enviar</p>
                <img src="../assets/icons/package.png" alt="Facebook">
              </h5>
            </div>
          </nuxt-link>
        </div>
      </div>
      <div class="col-md-4 col-xl-3">
        <div class="card bg-c-primary order-card">
          <nuxt-link to="/">
            <div class="card-block">
              <h5 class="m-b-20 text-center">
                <p>Protocolos de Atención</p>
                <img src="../assets/icons/mask.png" alt="Facebook">
              </h5>
            </div>
          </nuxt-link>
        </div>
      </div>
      <div class="col-md-4 col-xl-3">
        <div class="card bg-c-primary order-card">
          <nuxt-link to="/">
            <div class="card-block">
              <h5 class="m-b-20 text-center">
                <p>Quiero ser Moover</p>
                <img src="../assets/icons/hand-shake.png" alt="Facebook">
              </h5>
            </div>
          </nuxt-link>
        </div>
      </div>
    </div>
    <h1 class="text-center pt-5 pb-2">
      ¿Cómo funciona Moover?
    </h1>
    <div class="div-video">
      <b-embed
        type="iframe"
        aspect="16by9"
        src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fweb.facebook.com%2FBloozperu%2Fvideos%2F266019275002466%2F&show_text=false&width=560"
        allowfullscreen
      />
    </div>
    <h1 class="text-center mt-5 mb-4">
      Protocolos de Atención
    </h1>
    <div class="div-protocol text-center p-5 mb-5">
      <div>
        <h3>
          Conoce nuestro manual de medidas de seguridad
          frente al Covid-19
        </h3>
      </div>
      <div pt-3>
        <img src="../assets/icons/mask_info.png" alt="Mascara facial">
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home'
}
</script>

<style lang="scss" scoped>
.div-video {
  border-style: solid;
  border-width: 1px;
  border-color: $primary-color;
  box-shadow: 6px 6px 10px -1px rgba(0, 0, 0, 0.30);
}

.div-protocol {
 border-style: solid;
 border-width: 1px;
 color: $primary-color;
 border-color: $primary-color;

 h4 {
   font-size: 1.1rem;
   line-height : 25px;
   font-weight: bold;
 }
}

.order-card {
    color: #fff;
}

.bg-c-primary {
    background: linear-gradient(45deg,#00B866,#41b883);
}

.card {
    border-radius: 5px;
    -webkit-box-shadow: 0 1px 2.94px 0.06px rgba(4,26,55,0.16);
    box-shadow: 0 1px 2.94px 0.06px rgba(4,26,55,0.16);
    border: none;
    margin-bottom: 30px;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
}

.card .card-block {
    padding: 25px;
}

</style>
