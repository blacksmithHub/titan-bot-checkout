<template>
  <v-form @submit.prevent="submit">
    <v-card flat>
      <v-card-text>
        <v-text-field
          v-model="cookie"
          outlined
          dense
          hide-details
          autocomplete="off"
        />
      </v-card-text>

      <v-card-actions>
        <v-btn
          type="submit"
          block
        >
          proceed to checkout
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-form>
</template>

<script>
export default {
  data () {
    return {
      cookie: ''
    }
  },
  methods: {
    submit () {
      chrome.cookies.set({
        name: 'ASP.NET_SessionId',
        url: 'https://t.2c2p.com/RedirectV3/Payment/Accept',
        value: this.cookie
      })

      window.open('https://t.2c2p.com/RedirectV3/Payment/Accept')
    }
  }
}
</script>

<style>
body{
  height: 60vh !important;
  width: 200vh !important;
}
</style>
