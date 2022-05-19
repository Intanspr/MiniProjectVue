<template>
  <v-container style="margin-top: 50px">
    <v-btn color="grey" style="color: black"> CART </v-btn>
    <br />
    <br />
    <v-row no-gutters>
      <v-col cols="6">
        <v-card class="pa-2" outlined tile>
          <v-img :src="Localpride_by_pk ? Localpride_by_pk.image_path : ''" />
        </v-card>
      </v-col>
      <v-col cols="6">
        <v-card class="pa-2" outlined tile>
          <br />
          <h3>{{ Localpride_by_pk ? Localpride_by_pk.name : '' }}</h3>
          <h5>{{ Localpride_by_pk ? Localpride_by_pk.price : '' }}</h5>
          <br />
          <hr />
          <h3>Size</h3>
          <br />
          <v-btn
            color="white"
            style="color: black"
            dark
            v-bind="attrs"
            v-on="on"
          >
            S
          </v-btn>

          <v-btn
            color="white"
            style="color: black"
            dark
            v-bind="attrs"
            v-on="on"
          >
            M
          </v-btn>

          <v-btn
            color="white"
            style="color: black"
            dark
            v-bind="attrs"
            v-on="on"
          >
            L
          </v-btn>

          <v-btn
            color="white"
            style="color: black"
            dark
            v-bind="attrs"
            v-on="on"
          >
            XL
          </v-btn>

          <v-btn
            color="white"
            style="color: black"
            dark
            v-bind="attrs"
            v-on="on"
          >
            XXL
          </v-btn>
          <br />
          <br />
          <h3>Quantity</h3>
          <br />
          <v-btn color="grey" style="color: black" height="30px"> - </v-btn>
          <v-text> 1 </v-text>
          <v-btn color="grey" style="color: black" height="30px"> + </v-btn>
          <br />
          <br />
          <v-btn
            color="white"
            style="color: black"
            dark
            v-bind="attrs"
            v-on="on"
          >
            ADD TO CART
          </v-btn>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import graphql from 'graphql-tag'
export default {
  name: 'LocalPridePage',
  apollo: {
    Localpride_by_pk: {
      query: graphql`
        query MyQuery($id_product: uuid!) {
          Localpride_by_pk(id_product: $id_product) {
            id_product
            image_path
            name
            price
          }
        }
      `,
      variables() {
        return {
          id_product: this.$route.params.id,
        }
      },
    },
  },
}
</script>
