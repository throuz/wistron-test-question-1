<template>
  <v-form v-model="valid">
    <v-row>
      <v-col cols="3">
        <v-text-field
          v-model="carID"
          :rules="[(v) => !!v || 'Name is required']"
          label="Car ID"
          required
        />
      </v-col>
      <v-col cols="3">
        <v-select
          v-model="select"
          :items="prodIDs"
          :rules="[(v) => !!v || 'Prod ID is required']"
          label="Prod ID"
          required
        ></v-select>
      </v-col>
      <v-col cols="3">
        <v-text-field
          v-model="testName"
          :rules="[(v) => !!v || 'Test Name is required']"
          label="Test Name"
          required
        />
      </v-col>
      <v-col cols="3" class="d-flex align-center">
        <v-btn block class="mr-4">Query</v-btn>
      </v-col>
    </v-row>
  </v-form>
</template>

<script>
import { info } from "@/mock/data.js";

export default {
  name: "Search",

  data: () => ({
    valid: false,
    carID: "",
    select: null,
    prodIDs: [],
    testName: "",
  }),

  created() {
    this.carID = info["Car ID"];
    this.prodIDs = info["Prod ID"];
    this.testName = info["Test Name"];
  },
};
</script>
