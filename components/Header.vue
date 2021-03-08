<template>
  <header>
    <b-navbar toggleable="md" type="" variant="light">
      <b-container>
        <b-navbar-brand>
          <nuxt-link to="/">
            <img class="logo" src="../assets/icons/logo.jpg" alt="logo">
          </nuxt-link>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse" />

        <b-collapse id="nav-collapse" class="links" is-nav>
          <b-navbar-nav>
            <b-nav-item>
              <nuxt-link to="/">
                <p>Inicio</p>
              </nuxt-link>
            </b-nav-item>
            <b-nav-item>
              <nuxt-link to="/tracking">
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
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
.logo {
  width: 4rem;
}

.links {
  justify-content: flex-end;
}
</style>
