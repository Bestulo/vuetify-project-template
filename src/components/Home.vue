<template lang="pug">
  v-content
    // Banner
    // Banner
    // Banner
    // Banner
    v-container(grid-list-md text-xs-center)
      v-layout(row wrap)
        v-flex(xs12)
          v-card(dark color="primary")
            v-card-text(class="px-0") 12
    v-card(img="https://i.imgur.com/v7cphp0.jpg")
</template>

<script>
import Banner from '@/components/Banner'
export default {
  components: {
    Banner
  }
}
</script>
