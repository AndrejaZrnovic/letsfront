<template>
  <v-footer
    v-bind="localAttrs"
    :padless="padless"
    width="100%"
    class="pa-0"
    >
    <v-card
      flat
      tile
      width="100%"
      class="text-center"
      color="#ffb32a" 
      >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          icon
          >
          <v-icon size="40px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>
      <v-divider></v-divider>
    </v-card>
  </v-footer>
</template>


<script>
export default {
    name:'Footer',
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-instagram',
      ],
    }),
 
  }
</script>

<style scoped lang="scss">


</style>
