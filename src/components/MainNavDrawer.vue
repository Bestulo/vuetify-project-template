<template lang="pug">

  -
    const navClasses = [
      "blue",
      "darken-2",
      "hiden-sm-and-down"
    ]

  v-navigation-drawer#MainNavDrawer(
    class = navClasses
    app
    dark
    clipped
    fixed
    mobile-break-point=600
    style="display:flex;flex-direction:column;") <!-- .brown(dark) -->
    v-divider
    v-list(dense='' class="pt-0")
      v-list-tile(
        v-for="item in hiddenItems"
        :key="item.title"
        v-ripple=''
        @click="setRoute(item.path, $event)").hidden-sm-and-up
        v-list-tile-action
          v-icon {{ item.icon }}
        v-list-tile-content
          v-list-tile-title {{ item.title }}
      v-list-tile(
        v-for="item in items"
        :key="item.title"
        v-ripple=''
        @click="setRoute(item.path, $event)")
        v-list-tile-action
          v-icon {{ item.icon }}
        v-list-tile-content
          v-list-tile-title {{ item.title }}
      v-spacer
      v-list-tile
        v-list-tile-action
          v-icon <!-- an icon for Productos -->
        v-list-tile-title Productos
      v-divider
      v-list-group
        // do stuff here with activators like this https://vuetifyjs.com/en/components/navigation-drawers#nested-lists
        // Maybe make Productos open the product section, where we would have Cacao -> Semillas / Otros | Chocolate -> This / That | etc.
    v-spacer
    v-divider
    div
      .container(style="display:flex;margin-left:15px;")
        div
          h5.text-center.subheading.font-weight-light.ml-3.white--text Síguenos
          v-btn(icon).blue
            v-icon mdi-twitter
          v-btn(icon).pink.darken-3
            v-icon mdi-instagram
        div
          h5.text-center.subheading.font-weight-light.ml-3.white--text Háblanos
          v-btn(icon).green.darken-1
            v-icon mdi-whatsapp
          v-btn(icon).blue
            v-icon mdi-telegram
</template>

<script>
export default {
  data () {
    return {
      items: [
        { path: '/life', title: 'Life', icon: 'dashboard' },
        { path: '/death', title: 'Death', icon: 'question_answer' }
      ],
      hiddenItems:[
        { path: '/contactanos', title: 'Contáctanos', icon: 'mdi-email-outline' },
        { path: '/carrito', title: 'Tu Carrito', icon: 'mdi-cart-outline' }
      ],
      right: null,
      mini: false,
      smaller: window.innerWidth <= 600
    }
  },
  created () {
    this.handleResize();
  },
  methods: {
    setRoute (a, evt) {
      this.$router.push(a)
    }
  }
}

window.addEventListener('resize', this.handleResize)
const handleResize = () => {
  this.smaller = window.innerWidth <= 600
}

</script>

<style lang="stylus">
</style>
