<template>
  <v-footer padless>
    <v-card class="flex" flat tile>
      <v-card-title style="color: white">
        <div style="display: inline-block">
          <span>Contact US</span>
          <v-divider></v-divider>
          <span>How To Shop</span>
          <v-divider></v-divider>
          <span>FAQ</span>
          <v-divider></v-divider>
          <span>Payment Confirmation</span>
          <v-divider></v-divider>
          <span>Refund Policy</span>
        </div>

        <v-spacer></v-spacer>

        <v-img
          src="https://i.postimg.cc/KjmNqZKJ/1625492037799-1.png"
          max-width="120"
          max-height="120"
        />
        <br />
        <span>FIND US ON</span>
        <v-btn v-for="icon in icons" :key="icon" class="mx-4 pt-4" dark icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        Copyright &copy; 2020-2022 — <strong>SUNDS.CO</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin', 'mdi-instagram'],
  }),
}
</script>
