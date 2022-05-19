<template>
  <v-container>
    <br />
    <br />
    <div class="my-2">
      <v-btn color="black" dark large> T-SHIRT </v-btn>
    </div>
    <v-row>
      <v-col v-for="item in Allproduct" :key="item.id_product" cols="4">
        <br />
        <br />
        <v-card class="mx-auto" max-width="400">
          <v-img :src="item.image_path" height="400px"></v-img>

          <v-card-title>
            {{ item.price }}

            <v-spacer />
            <NuxtLink :to="`/detail/${item.id_product}`"
              ><v-btn
                small
                replace
                color="grey"
                v-bind="item.image_path"
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
  name: 'AllPage',
  apollo: {
    Allproduct: graphql`
      query MyQuery {
        Allproduct {
          id_product
          image_path
          price
        }
      }
    `,
  },
}
</script>
