<template>
  <footer class="pt-5 pb-2 footer">
    <div class="container">
      <div class="row">
        <div class="col-lg-5 col-xs-12 contact">
          <h2>¿Necesitas hablar con el equipo Moover?</h2>
          <p class="mt-5">
            <nuxt-link to="/contact">
              CONTÁCTANOS
            </nuxt-link>
          </p>
        </div>
        <div class="col-lg-3 col-xs-12">
          <p>Quienes somos</p>
          <p>Términos de condiciones</p>
          <p>Trabaja con nosotros</p>
        </div>
        <div class="col-lg-4 col-xs-12 social-media">
          <h4 class="mt-lg-0 mt-sm-4 mb-4">
            Síguenos
          </h4>
          <a href="https://www.linkedin.com/company/blooz/about/" target="_blank"><img src="../assets/icons/linkedin_white.png" alt="LinkedIn"></a>
          <a href="https://web.facebook.com/Bloozperu" target="_blank"><img src="../assets/icons/facebook_white.png" alt="Facebook"></a>
          <a href="https://www.instagram.com/bloozperu/" target="_blank"><img src="../assets/icons/instagram_white.png" alt="Instagram"></a>
          <a href="https://www.blooz.pe/" target="_blank"><img src="../assets/icons/twitter_white.png" alt="Twitter"></a>
        </div>
      </div>
      <div class=" mt-5">
        <div class="copyright">
          <p>
            <small class="text-white-50">All Rights Reserved © 2021</small>
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss" scoped>
.footer{
  color: $white;
  background: $secondary-color;

  .copyright {
    text-align: center;
    p {
      border-top:1px solid rgba(255,255,255,.1);
      }
  }
}
</style>
