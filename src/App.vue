<template>
  <v-app>
    <v-main>
      <v-container fluid fill-height class="justify-center">
        <v-card style="width:300px">
          <v-card-text>
            <v-menu offset-y v-model="menu">
              <template #activator="{on}">
                <v-text-field
                  v-on="on"
                  label="click to select icon"
                  hide-details
                  :prepend-inner-icon="selected"
                  v-model="selected"
                  single-line
                >
                </v-text-field>
              </template>
              <v-card @click.stop.native flat>
                <icon-picker v-model="selected" height="200" />
              </v-card>
            </v-menu>
          </v-card-text>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import IconPicker from "./components/IconPicker.vue";

export default {
  name: "App",
  components: {
    IconPicker
  },
  data: () => ({
    selected: "",
    menu: false
  })
};
</script>

<style>
html {
  overflow: auto;
}
</style>
