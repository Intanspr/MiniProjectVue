<template>
  <v-container>
    <br />
    <br />
    <div class="my-2">
      <v-btn color="black" dark large> LOCAL PRIDE </v-btn>
    </div>
    <v-row>
      <v-col v-for="local in Localpride" :key="local.id_product" cols="6">
        <br />
        <br />
        <v-card class="mx-auto" max-width="500">
          <v-img :src="local.image_path" height="500px"></v-img>

          <v-card-title>
            {{ local.price }}

            <v-spacer />
            <NuxtLink :to="`/detail/${local.id_product}`"
              ><v-btn
                small
                replace
                color="grey"
                v-bind="local.image_path"
                target="_blank"
              >
                More Detail
              </v-btn></NuxtLink
            >
          </v-card-title>
        </v-card>
      </v-col>
    </v-row>
    <Young />
  </v-container>
</template>

<script>
import graphql from 'graphql-tag'
export default {
  name: 'LocalPage',
  apollo: {
    Localpride: graphql`
      query MyQuery {
        Localpride {
          id_product
          image_path
          price
        }
      }
    `,
  },
}
</script>
