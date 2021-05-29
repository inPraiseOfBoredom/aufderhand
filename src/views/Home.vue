<template>
  <v-app>
    <v-content>
      <div class="home">
        <v-tabs v-model="tab" fixed-tabs background-color="pink">
          <v-tab v-for="item in items" :key="item">
            {{ item }}
          </v-tab>
        </v-tabs>

        <Calendar />
      </div>
    </v-content>
  </v-app>
</template>

<script>
// @ is an alias to /src
import Calendar from "@/components/Calendar.vue";
export default {
  name: "Home",
  components: {
    Calendar,
  },
  data() {
    return {
      tab: null,
      items: ["Meal plan", "ingredients", "shopping list"],
    };
  },
};
</script>

<style scoped></style>
