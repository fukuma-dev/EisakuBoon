<template>
  <v-app>
    <custom-header v-if="$route.name !== 'index'" />
    <nuxt />
  </v-app>
</template>

<script>
export default {
  components: {
    CustomHeader: () => import('~/components/TheHeader.vue')
  }
}
</script>
