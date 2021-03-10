<template>
  <header>
    <b-navbar toggleable="md" variant="light" class="nav-bar">
      <b-container>
        <b-navbar-brand>
          <nuxt-link to="/">
            <img class="logo-nav" src="../assets/icons/logo_nav.jpg" alt="logo">
          </nuxt-link>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse" />

        <b-collapse id="nav-collapse" class="links" is-nav>
          <b-navbar-nav>
            <b-nav-item>
              <nuxt-link to="/">
                Inicio
              </nuxt-link>
            </b-nav-item>
            <b-nav-item>
              <nuxt-link v-b-modal.modal-2 to="/tracking">
                Seguimiento
              </nuxt-link>
            </b-nav-item>
            <b-nav-item>
              <nuxt-link to="/registerOrder">
                Registrar orden
              </nuxt-link>
            </b-nav-item>
            <b-nav-item>
              <nuxt-link to="/contact">
                Contáctanos
              </nuxt-link>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
    <b-modal
      id="modal-2"
      title="Seguimiento de envío"
      @ok="showTracking($event)"
    >
      <p class="mt-2">
        Por favor, ingrese su numero de orden: {{ order }}
      </p>
      <input v-model="order" placeholder="N° de Orden">
    </b-modal>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {

    }
  },
  methods: {
    showTracking () {
      // alert('click')
    }
  }

}
</script>

<style lang="scss" scoped>

.nav-bar {
  box-shadow: 0 2px 4px 0 rgba(0,0,0,.2);

  .nav-link {
    text-align: center;
      &:hover{
        background: $primary-color;
      }
  }

  // .navbar-toggler-icon {
  //   background-image: url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 32 32' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba(65,184,131, 0.5)' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 8h24M4 16h24M4 24h24'/%3E%3C/svg%3E");
  // }
}

.logo-nav {
  width: 4rem;
}

.links {
  justify-content: flex-end;

}
</style>
