<template>
  <div class="tracking-container">
    <h2 class="text-center mt-5 mb-4">
      Seguimiento de Envío
    </h2>
    <!-- PROGRESS-BAR -->
    <div class="container px-1 px-md-4 mt-3 pb-5 mx-auto">
      <div class="card mt-0 mb-0 bg-light">
        <div class="col d-flex flex-column px-3 top">
          <div class="text-center font-weight-bold">
            <h3>N° de Orden: 07810</h3>
          </div>
          <div class="d-flex flex-column text-sm-right pt-3">
            <p class="mb-0 font-weight-bold bg-light">
              Ultima Actualización
            </p>
            <p class="bg-light">
              <span class="font-weight-bold">Fecha:</span>
              05/03/21
              <span class="font-weight-bold">Hora:</span>
              13:00pm
            </p>
          </div>
        </div> <!-- Agregando clase 'active' a progreso -->
        <div class="row d-flex justify-content-center">
          <div class="col-12">
            <ul id="progressbar" class="text-center">
              <li class="active step0" />
              <li class="active step0" />
              <li class="active step0" />
              <li class="step0" />
            </ul>
          </div>
        </div>
        <div class="row justify-content-between top mx-0">
          <div class="row d-flex icon-content">
            <img class="icon" src="../assets/icons/register_track.png">
            <div class="d-flex justify-content-end flex-column">
              <p class="font-weight-bold">
                Registro
              </p>
            </div>
          </div>
          <div class="row d-flex icon-content">
            <img class="icon" src="../assets/icons/package_track.png">
            <div class="d-flex flex-column justify-content-end">
              <p class="font-weight-bold">
                Recepcionado
              </p>
            </div>
          </div>
          <div class="row d-flex icon-content">
            <img class="icon" src="../assets/icons/transit_track.png">
            <div class="d-flex flex-column justify-content-end">
              <p class="font-weight-bold">
                En tránsito
              </p>
            </div>
          </div>
          <div class="row d-flex icon-content">
            <img class="icon" src="../assets/icons/end_track.png">
            <div class="d-flex flex-column justify-content-end">
              <p class="font-weight-bold">
                Entregado
              </p>
            </div>
          </div>
        </div>
        <div class="container">
          <b-table hover :items="items" class="mt-4 text-center" />
        </div>
      </div>
    </div>
    <!-- END-PROGRESS-BAR -->
  </div>
</template>

<script>
export default {
  name: 'Tracking',
  data () {
    return {
      items: [
        { Fecha: '05/03/2021', Hora: '11:45', Actividad: 'Envío en tránsito' },
        { Fecha: '05/03/2021', Hora: '11:30', Actividad: 'Envío recepcionado por el Moover' },
        { Fecha: '05/03/2021', Hora: '11:10', Actividad: 'Moover en tránsito a recoger envío' },
        { Fecha: '05/03/2021', Hora: '10:50', Actividad: 'Asignando conductor Moover' },
        { Fecha: '05/03/2021', Hora: '10:30', Actividad: 'Registro de orden' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

.tracking-container {
  h2 {
    color: $primary-color;
  }
}

.card {
    z-index: 0;
    padding-bottom: 20px;
    margin-top: 90px;
    margin-bottom: 90px;
    border-style: solid;
    border-width: 1px;
    border-color: $primary-color;
    border-radius: 2rem;
    box-shadow: 6px 6px 10px -1px rgba(0, 0, 0, 0.30);
}

.top {
    padding-top: 40px;
    padding-left: 13% !important;
    padding-right: 13% !important;
}

#progressbar {
    margin-bottom: 30px;
    overflow: hidden;
    color: #78B89C;
    padding-left: 0px;
    margin-top: 30px
}

#progressbar li {
    list-style-type: none;
    font-size: 13px;
    width: 25%;
    float: left;
    position: relative;
    font-weight: 400
}

#progressbar .step0:before {
    content: "✔";
    color: $white
}

#progressbar li:before {
    width: 40px;
    height: 40px;
    line-height: 45px;
    display: block;
    font-size: 20px;
    background: #C5CAE9;
    border-radius: 50%;
    margin: auto;
    padding: 0px
}

#progressbar li:after {
    content: '';
    width: 100%;
    height: 12px;
    background: #C5CAE9;
    position: absolute;
    left: 0;
    top: 16px;
    z-index: -1
}

#progressbar li:last-child:after {
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px;
    position: absolute;
    left: -50%
}

#progressbar li:nth-child(2):after,
#progressbar li:nth-child(3):after {
    left: -50%
}

#progressbar li:first-child:after {
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px;
    position: absolute;
    left: 50%
}

#progressbar li:last-child:after {
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px
}

#progressbar li:first-child:after {
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px
}

#progressbar li.active:before,
#progressbar li.active:after {
    background: $primary-color;
}

#progressbar li.active:before {
    content:"✔"
}

.icon {
    width: 35px;
    height: 35px;
    margin-right: 10px
}

.icon-content {
    padding-bottom: 20px
}

@media screen and (max-width: 992px) {
    .icon-content {
        width: 50%
    }
}
</style>
