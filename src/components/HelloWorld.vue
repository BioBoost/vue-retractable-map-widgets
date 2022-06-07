<template>

<v-container>  
    <v-row no-gutters>
      <v-col cols="12">
        <v-card class="d-flex flex-column pa-3 bg-grey-lighten-4">
          <v-card-title class="justify-center">
            {{ widgets[0].value }}
          </v-card-title>
        </v-card>
      </v-col>

      <v-col cols="12">
        <v-expansion-panels>
          <v-expansion-panel>
            <v-expansion-panel-title class="d-flex justify-center align-center" hide-icons>
              <v-icon color="error" icon="mdi-map-marker" class="mr-4"></v-icon> Click to toggle the map 
            </v-expansion-panel-title>
            <v-expansion-panel-text>
              <v-img src="https://media.wired.com/photos/59269cd37034dc5f91bec0f1/191:100/w_1280,c_limit/GoogleMapTA.jpg" />
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
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
  }),
}
</script>