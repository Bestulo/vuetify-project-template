<template lang="pug">

  - const logoPath = '@/assets/logo-white.png'

  v-toolbar.my-toolbar.blue.darken-3(dark app clipped-left) <!-- (color='brown' dark) -->
    v-toolbar-side-icon#Hamburger.hidden-sm-and-up <!-- hamburger-->
    v-toolbar-title
      router-link(to="/")
        img(src=logoPath alt="Master of Dao" width="200" style="vertical-align:middle")
        // | I include thee!
    v-spacer
    v-toolbar-items.hidden-xs-only
      // Default icons before md
      v-btn(flat) Productos
      v-btn(flat) Vender

      // Icons sm and down
      v-btn(flat).hidden-sm-and-down
        v-icon(left dark) mdi-email-outline
        | Contáctanos
      v-btn(flat).hidden-sm-and-down
        v-icon(left dark) mdi-cart-outline
        | Tu carrito

      // Icons md and up
      v-btn(flat icon dark).hidden-md-and-up
        v-icon(dark) mdi-email-outline
      v-btn(flat icon dark).hidden-md-and-up
        v-icon(dark) mdi-cart-outline

</template>

<style lang="stylus">
  .my-toolbar
    z-index:4
</style>
