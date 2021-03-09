<template>
  <div class="contact-container pt-3">
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
      <div class="div-logo d-flex align-items-center py-2 px-5">
        <img class="logo" src="../assets/icons/logo.jpg" alt="logo">
      </div>
    </div>
    <div class="container form-contact py-3 my-5 ">
      <h4 class="text-center font-weight-bold pt-5 pb-4">
        CONTÁCTANOS
      </h4>
      <b-form v-if="show" @submit="onSubmit" @reset="onReset">
        <b-form-group id="input-group-1" label="Nombres:" label-for="input-1">
          <b-form-input
            id="input-1"
            v-model="form.name"
            placeholder=""
            required
          />
        </b-form-group>

        <b-form-group id="input-group-2" label="Apellidos:" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.lastName"
            placeholder=""
            required
          />
        </b-form-group>

        <b-form-group id="input-group-3" label="Correo:" label-for="input-3">
          <b-form-input
            id="input-3"
            v-model="form.email"
            type="email"
            placeholder=""
            required
          />
        </b-form-group>

        <b-form-group id="input-group-4" label="Celular:" label-for="input-4">
          <b-form-input
            id="input-4"
            v-model="form.phone"
            placeholder=""
            required
          />
        </b-form-group>

        <!-- <b-form-group id="input-group-4" v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            id="checkboxes-4"
            v-model="form.checked"
            :aria-describedby="ariaDescribedby"
          > -->

        <b-form-group id="input-group-4">
          <b-form-checkbox-group>
            <b-form-checkbox value="security">
              He leido y aceptado la política de seguridad
            </b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>
        <div class="text-center py-4">
          <b-button class="btn-contact" type="submit" variant="primary">
            Enviar
          </b-button>
          <!-- <b-button type="reset" variant="danger">
            Cancelar
          </b-button> -->
        </div>
      </b-form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data () {
    return {
      form: {
        email: '',
        name: '',
        food: null,
        checked: []
      },
      foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
      show: true
    }
  },
  methods: {
    onSubmit (event) {
      event.preventDefault()
      // alert(JSON.stringify(this.form))
      alert('Gracias por contactarnos!')
    },
    onReset (event) {
      event.preventDefault()
      // Reset our form values
      this.form.name = ''
      this.form.lastName = ''
      this.form.email = null
      this.form.phone = ''
      this.form.checked = []
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>

<style lang="scss" scoped>

.container {
   max-width: 100vh;
}

.contact-text {
  background-color: $primary-color;
  border-top-left-radius: 80px 100px;
  border-bottom-right-radius: 80px 100px;
  justify-content: center;
  align-items: center;
  h6 {
    font-size: 1.1rem;
    line-height : 25px;
  }
}

.logo {
  width: 100%;
}

.form-contact {
  color: $primary-color;
  border-style: solid;
  border-width: 1px;
  border-color: $primary-color;
  border-radius: 2rem;
  box-shadow: 6px 6px 10px -1px rgba(0, 0, 0, 0.30);
}

.btn-contact {
  width: 20rem;
}

</style>
