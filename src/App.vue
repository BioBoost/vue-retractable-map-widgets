<template>
  <v-app>
    <v-app-bar color="green">
      <v-app-bar-title class="font-weight-bold">Demo of Retractable Map Navigator</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn flat size="large" prepend-icon="mdi-human-greeting-proximity">Contact Us</v-btn>

    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>

    <v-footer
      bottom
      color="green"
      class="text-center d-flex flex-column"
    >
      <v-row class="my-5">
        <v-col cols="12">
          <div class="text-h4">
            <v-icon size="x-small">mdi-rocket-launch</v-icon>
              Where demo's become reality
            <v-icon size="x-small">mdi-rocket-launch</v-icon>
          </div>
        </v-col>  
      </v-row>

      <v-row>
        <v-col cols="12" sm="4">
          <v-card tile flat color="transparent">
            <v-card-title class="justify-center">Founded in 2019</v-card-title>
            <v-card-text>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maxime non vel itaque odio sit debitis culpa animi aspernatur vero suscipit, cum incidunt iure dignissimos a, nobis quis ipsa, repellendus nihil.
            </v-card-text>
            <v-container class="mt-4">
              <a href="https://www.vives.be" target="_blank">
                <v-img src="https://www.vives.be/sites/default/files/styles/banner/public/uploads/images/VIVES_LogoNewSmile.png?itok=0BtQiClI" max-height="80" contain></v-img>
              </a>
            </v-container>
          </v-card>
        </v-col>
        
        <v-col cols="12" sm="4">
          <v-card tile flat color="transparent">
            <v-card-title class="justify-center">Social Media</v-card-title>
            <div class="mt-4">
              <v-btn
                v-for="media in social_media"
                :key="media.icon"
                class="mx-4 white--text"
                icon flat
                color="transparent"
                :href="media.url"
                target="_blank"
              >
                <v-icon size="48px">{{ media.icon }}</v-icon>
              </v-btn>
            </div>
          </v-card>
        </v-col>
        
        <v-col cols="12" sm="4">
          <v-card tile flat color="transparent">
            <v-card-title class="justify-center">Placeholder</v-card-title>
            <v-card-text>
              Just a placeholder for something, who knows what?
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data() {
      return {
          social_media: [
              { icon: "mdi-facebook", url: "https://www.facebook.com/vivesiwt" },
              { icon: "mdi-linkedin", url: "https://www.linkedin.com/groups/8811012/" },
          ]
      };
  },
}
</script>
