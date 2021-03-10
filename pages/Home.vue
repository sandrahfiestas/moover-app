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
  </div>
</template>

<script>

export default {
  name: 'Home'
}
</script>

<style lang="scss" scoped>

// .div-slide{
//  width: 100vh;
// }

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
