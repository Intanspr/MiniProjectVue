<template>
  <v-container>
    <v-card>
      <br />
      <h1 class="text-md-h4 text-h6 text-center" style="color: white">
        BEST SELLER
      </h1>
      <br />
      <v-row>
        <v-col cols="4">
          <v-img src="https://i.postimg.cc/bNKnrCmT/IMG-20210530-WA0038.jpg" />
        </v-col>

        <v-col cols="4">
          <v-img src="https://i.postimg.cc/DfSdzX27/IMG-20210530-WA0025.jpg" />
        </v-col>

        <v-col cols="4">
          <v-img src="https://i.postimg.cc/cH233Fs0/IMG-20210530-WA0016.jpg" />
        </v-col>
      </v-row>

      <br />
      <div class="text-center">
        <NuxtLink to="/T-shirt">
          <v-btn rounded color="white" style="color: black"> T-shirt </v-btn>
        </NuxtLink>
        <NuxtLink to="/LocalPride">
          <v-btn rounded color="white" style="color: black">
            Local Pride
          </v-btn>
        </NuxtLink>
      </div>
      <br />
    </v-card>
  </v-container>
</template>
