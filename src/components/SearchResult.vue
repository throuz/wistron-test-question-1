<template>
  <v-row>
    <v-col>
      <v-tabs v-model="tabName">
        <v-tab v-for="item in tabNames" :key="item">
          {{ item }}
        </v-tab>
      </v-tabs>
      <v-tabs-items v-model="tabName">
        <v-tab-item v-for="(content, i) in contents" :key="i">
          <v-card color="basil" flat>
            <v-card-text>{{ content }}</v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-col>
  </v-row>
</template>

<script>
import { tab, base, detail } from "@/mock/data.js";

export default {
  name: "Search",

  data: () => ({
    tabName: null,
    tabNames: [],
    contents: [],
  }),

  created() {
    this.tabNames = tab;
    this.contents = [base[0].data, detail[0].data];
  },
};
</script>
