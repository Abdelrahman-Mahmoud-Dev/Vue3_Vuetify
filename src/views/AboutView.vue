<template>
  <div class="about">
    <v-card class="mx-auto" max-width="300">
      <v-list :items="items"></v-list>
    </v-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          title: "Item #1",
          value: 1,
        },
        {
          title: "Item #2",
          value: 2,
        },
        {
          title: "Item #3",
          value: 3,
        },
      ],
    };
  },
};
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
