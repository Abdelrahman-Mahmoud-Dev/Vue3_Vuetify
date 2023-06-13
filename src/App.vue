<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
</script>
<template>
  <v-card>
    <v-layout>
      <div>
        <v-toolbar density="compact">
          <v-app-bar-nav-icon
            v-if="this.$vuetify.display.mobile"
            @click.stop="drawer = !drawer"
          ></v-app-bar-nav-icon>

          <v-toolbar-title>Title</v-toolbar-title>
          <v-toolbar-title>Title</v-toolbar-title>
          <v-toolbar-title>Title</v-toolbar-title>
          <v-toolbar-title>Title</v-toolbar-title>
          <v-toolbar-title>Title</v-toolbar-title>
          <v-toolbar-title>Title</v-toolbar-title>
        </v-toolbar>
      </div>

      <v-navigation-drawer v-model="drawer" rail>
        <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Sandra Adams"
            subtitle="sandra_a88@gmailcom"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item
            prepend-icon="mdi-close"
            title="My Files"
            value="myfiles"
            @click="drawer = false"
          ></v-list-item>
          <v-list-item
            prepend-icon="mdi-folder"
            title="My Files"
            value="myfiles"
          ></v-list-item>

          <v-list-item
            prepend-icon="mdi-account-multiple"
            title="Shared with me"
            value="shared"
          ></v-list-item>
          <v-list-item
            prepend-icon="mdi-star"
            title="Starred"
            value="starred"
          ></v-list-item>
        </v-list>
      </v-navigation-drawer>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  created() {
    console.log("created", this.$vuetify.display.mobile);
  },
  data: () => ({
    drawer: false,
    group: null,
    items: [
      {
        title: "Foo",
        value: "foo",
      },
      {
        title: "Bar",
        value: "bar",
      },
      {
        title: "Fizz",
        value: "fizz",
      },
      {
        title: "Buzz",
        value: "buzz",
      },
    ],
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>

<style scoped></style>
