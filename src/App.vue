<template>
  <v-app>
    <v-app-bar app color="black" dark>
      <div class="d-flex align-center">
        <h2>3DAYC</h2>
      </div>

      <v-spacer></v-spacer>

      <v-btn :href="link.instagram" target="_blank" text style="padding:0">
        <span class="mr-2">INSTAGRAM</span>
        <v-icon>{{ icons.mdiShareVariant }}</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <Modal openText="Click" closeText="close" />
      <Card />
      <List />
    </v-main>
  </v-app>
</template>

<script>
import { mdiShareVariant } from "@mdi/js";
import Card from "./components/Card";
import List from "./components/List";
import Modal from "./components/Modal";

export default {
  name: "App",

  components: {
    Card,
    List,
    Modal,
  },

  data: () => ({
    icons: {
      mdiShareVariant,
    },
    link: {
      instagram: "https://www.instagram.com/3dayc/",
    },
  }),
};
</script>

<style>
body {
  overflow: hidden;
}
</style>
