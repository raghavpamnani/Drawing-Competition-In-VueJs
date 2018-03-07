<template>
  <v-tabs
      v-model="active"
      color="cyan"
      dark
      slider-color="yellow"
    >
      <v-tab
        ripple
      >LoginIn
      </v-tab>
      <v-tab
        ripple
      >Sign Up
      </v-tab>
      <v-tab-item>
        <login></login>
      </v-tab-item>
      <v-tab-item>
        <login></login>
      </v-tab-item>
</v-tabs>
</template>

<script>
  export default {
    data () {
      return {
        active: null,
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
      }
    },
    methods: {
      next () {
        const active = parseInt(this.active)
        this.active = (active < 2 ? active + 1 : 0).toString()
      }
    }
  }
</script>

