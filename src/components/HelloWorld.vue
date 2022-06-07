<template>
  <v-sheet>
    <v-row dense>

      <v-col cols="auto">
        <v-card color="primary" class="d-flex justify-center align-center rounded-0" height="100%" hover @click="show_map=!show_map">
          <v-icon class="mx-2" size="x-large">mdi-map-marker</v-icon>
        </v-card>
      </v-col>

      <v-col cols="11">
        <div>
        <v-dialog
          v-model="show_map"
        >
          <v-card>
            <v-card-title>Sensor Map</v-card-title>
              <v-img src="https://cdn.vuetifyjs.com/images/cards/forest-art.jpg" min-width="600"></v-img>
            <v-card-text>
              Please select a sensor from the map.
            </v-card-text>
          </v-card>
        </v-dialog>
        </div>

        <v-container>  

          <v-row>
            <v-col cols="12">
              <v-card class="d-flex flex-column pa-3 bg-grey-lighten-4">
                <v-card-title class="justify-center">
                  {{ widgets[0].value }}
                </v-card-title>
              </v-card>
            </v-col>
          </v-row>

          <v-row class="my-10">
            <v-col cols="12" class="text-center">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure ducimus accusamus iste quasi, quo cumque placeat minus quaerat voluptatibus eaque quia veritatis soluta voluptatum dolor, non optio quibusdam quidem blanditiis?
            </v-col>
          </v-row>

          <v-row align="center" justify="center">
            <v-col cols="12" sm="6" md="4" v-for="widget in widgets" :key="widget.title">
              <v-card color="grey-lighten-3 d-flex flex-column">
                <v-card-title class="justify-center">{{ widget.title }}</v-card-title>
                <v-card-text class="text-center"><v-icon size="x-large">{{ widget.icon }}</v-icon></v-card-text>
                <v-card-text class="text-center">{{ widget.value }}</v-card-text>
              </v-card>
            </v-col>

          </v-row>

          <v-row class="my-10">
            <v-col cols="12" class="text-center">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure ducimus accusamus iste quasi, quo cumque placeat minus quaerat voluptatibus eaque quia veritatis soluta voluptatum dolor, non optio quibusdam quidem blanditiis?
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure ducimus accusamus iste quasi, quo cumque placeat minus quaerat voluptatibus eaque quia veritatis soluta voluptatum dolor, non optio quibusdam quidem blanditiis?
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure ducimus accusamus iste quasi, quo cumque placeat minus quaerat voluptatibus eaque quia veritatis soluta voluptatum dolor, non optio quibusdam quidem blanditiis?
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure ducimus accusamus iste quasi, quo cumque placeat minus quaerat voluptatibus eaque quia veritatis soluta voluptatum dolor, non optio quibusdam quidem blanditiis?
            </v-col>
          </v-row>

        </v-container>
      </v-col>

    </v-row>
  </v-sheet>
</template>

<script>

export default {
  name: 'HelloWorld',

  data: () => ({
    widgets: [
      {
        title: "Name",
        value: "Soil Sensor Brugge",
        icon: 'mdi-ab-testing'
      },
      {
        title: "Type",
        value: "DUST-sensor",
        icon: 'mdi-crosshairs-question'
      },
      {
        title: "Moisture @ -12cm",
        value: "33%",
        icon: 'mdi-water'
      },
      {
        title: "Moisture @ -4cm",
        value: "12%",
        icon: 'mdi-water'
      },
      {
        title: "Moisture @ ground",
        value: "14%",
        icon: 'mdi-water'
      },
      {
        title: "Temperature",
        value: "14°C",
        icon: 'mdi-thermometer'
      },
      {
        title: "Location",
        value: "Spoorwegstraat 12 - Bruges",
        icon: 'mdi-map-marker'
      },
      {
        title: "Last Data",
        value: "12 seconds ago",
        icon: 'mdi-signal-variant'
      },
    ],
    show_map: false
  }),
}
</script>