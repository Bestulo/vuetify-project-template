<template lang="pug">
  #app
    v-app#inspire
      MainToolbar
      MainNavDrawer
      Home
        // v-container(fluid fill-height)
          // .v-layout(justify-center='' align-center='')
          //   h3 div.container &gt; h3

  // Banner

  // v-navigation-drawer(stateless='' value='true')
  //   v-list
  //     v-list-tile
  //       v-list-tile-action
  //         v-icon home
  //       v-list-tile-title Home
  //     v-list-group(prepend-icon='account_circle' value='true')
  //       template(v-slot:activator='')
  //         v-list-tile
  //           v-list-tile-title Users
  //       v-list-group(no-action='' sub-group='' value='true')
  //         template(v-slot:activator='')
  //           v-list-tile
  //             v-list-tile-title Admin
  //         v-list-tile(v-for='(admin, i) in admins' :key='i' @click='')
  //           v-list-tile-title(v-text='admin[0]')
  //           v-list-tile-action
  //             v-icon(v-text='admin[1]')
  //       v-list-group(sub-group='' no-action='')
  //         template(v-slot:activator='')
  //           v-list-tile
  //             v-list-tile-title Actions
  //         v-list-tile(v-for='(crud, i) in cruds' :key='i' @click='')
  //           v-list-tile-title(v-text='crud[0]')
  //           v-list-tile-action
  //             v-icon(v-text='crud[1]')
  // v-container
  //   Banner
</template>

<script>

import MainToolbar from '@/components/MainToolbar'
import MainNavDrawer from '@/components/MainNavDrawer'
import Home from '@/components/Home'

export default {
  // data () {
  //   return {
  //   }
  // },
  components: {
    MainToolbar,
    MainNavDrawer,
    Home
  }
}
</script>

<style lang="stylus">

</style>
