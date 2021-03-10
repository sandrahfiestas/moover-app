<template>
  <div class="form-container">
    <h2 class="text-center mt-5 mb-4">
      Registrar Orden
    </h2>
    <div class="container bg-light">
      <h5 class="py-4">
        ¿Dónde retiramos tu envío?
      </h5>
      <b-form v-if="show" class="font-weight-bold" @submit="onSubmit" @reset="onReset">
        <b-form-group
          id="input-group-1"
          label="Dirección:"
          label-for="input-1"
        >
          <b-form-input
            id="input-1"
            v-model="form.address"
            placeholder=""
            required
          />
        </b-form-group>

        <b-form-group
          id="input-group-2"
          label="Distrito:"
          label-for="input-2"
        >
          <b-form-select
            id="input-2"
            v-model="form.district"
            :options="districts"
            required
          />
        </b-form-group>

        <b-form-group
          id="input-group-3"
          label="Contácto:"
          label-for="input-3"
        >
          <b-form-input
            id="input-3"
            v-model="form.contact"
            placeholder=""
            required
          />
        </b-form-group>

        <b-form-group
          id="input-group-4"
          label="Celular:"
          label-for="input-4"
        >
          <b-form-input
            id="input-4"
            v-model="form.phone"
            placeholder=""
            required
          />
        </b-form-group>

        <h5>
          Ingresa dimensiones de tu envío
        </h5>

        <div class="packet-data pt-2 pb-3">
          <b-form-group
            id="input-group-5"
            label="Peso:"
            label-for="input-5"
            class="mx-2"
          >
            <b-form-input
              id="input-5"
              v-model="form.peso"
              placeholder=""
              required
            />
          </b-form-group>

          <b-form-group
            id="input-group-6"
            label="Largo:"
            label-for="input-6"
            class="mx-2"
          >
            <b-form-input
              id="input-6"
              v-model="form.largo"
              placeholder=""
              required
            />
          </b-form-group>

          <b-form-group
            id="input-group-7"
            label="Alto:"
            label-for="input-7"
            class="mx-2"
          >
            <b-form-input
              id="input-7"
              v-model="form.alto"
              placeholder=""
              required
            />
          </b-form-group>

          <b-form-group
            id="input-group-8"
            label="Ancho:"
            label-for="input-8"
            class="mx-2"
          >
            <b-form-input
              id="input-8"
              v-model="form.ancho"
              placeholder=""
              required
            />
          </b-form-group>
        </div>

        <h5>
          ¿Dónde entregamos tu envío?
        </h5>

        <b-form-group
          id="input-group-9"
          label="Dirección:"
          label-for="input-9"
        >
          <b-form-input
            id="input-1"
            v-model="form.addressDos"
            placeholder=""
            required
          />
        </b-form-group>

        <b-form-group
          id="input-group-10"
          label="Distrito:"
          label-for="input-10"
        >
          <b-form-select
            id="input-10"
            v-model="form.districtDos"
            :options="districts"
            required
          />
        </b-form-group>

        <b-form-group
          id="input-group-11"
          label="Contácto:"
          label-for="input-11"
        >
          <b-form-input
            id="input-11"
            v-model="form.contactDos"
            placeholder=""
            required
          />
        </b-form-group>

        <b-form-group
          id="input-group-12"
          label="Celular:"
          label-for="input-12"
        >
          <b-form-input
            id="input-12"
            v-model="form.phoneDos"
            placeholder=""
            required
          />
        </b-form-group>
        <div class="div-btns-register">
          <b-button type="submit" variant="primary">
            Confirmar Despacho
          </b-button>
          <b-button type="reset" variant="danger">
            Cancelar
          </b-button>
        </div>
        <h6 class="pt-1 text-center text-danger">
          *Datos incorrectos, verifique por favor. Gracias
        </h6>
      </b-form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RegisterOrder',
  data () {
    return {
      form: {
        address: '',
        contact: '',
        phone: '',
        district: null,
        addressDos: '',
        contactDos: '',
        phoneDos: '',
        districtDos: null,
        checked: []
      },
      districts: [{ text: 'Seleccione distrito', value: null }, 'Ancón', 'Barranco', 'Breña', 'Carabayllo'],
      show: true
    }
  },
  methods: {
    onSubmit (event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    },
    onReset (event) {
      event.preventDefault()
      this.form.address = ''
      this.form.contact = ''
      this.form.phone = ''
      this.form.district = null
      this.form.addressDos = ''
      this.form.contactDos = ''
      this.form.phoneDos = ''
      this.form.districtDos = null
      this.form.checked = []
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>

<style lang="scss" scoped>

.form-container {
  h2, h5 {
    color: $primary-color
  }
  h6 {
    visibility: hidden;
  }
}

.container {
  max-width: 100vh;
  border-style: solid;
  border-width: 1px;
  border-color: $primary-color;
  border-radius: 2rem;
  margin-bottom: 10rem;
  box-shadow: 6px 6px 10px -1px rgba(0, 0, 0, 0.30);
}

.packet-data {
  display: flex;
  text-align: center;
}

.div-btns-register {
  display: flex;
  justify-content: center;
  padding-top: 1rem;
}

</style>
