<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="mb-4" cols="12">
        <h1 class="display-2 font-weight-bold mb-3">Production Data</h1>
      </v-col>
      <v-col class="mb-5" cols="12">
        <h2 class="headline font-weight-bold mb-3">Information</h2>
        <Search />
        <SearchResult />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Search from "@/components/Search.vue";
import SearchResult from "@/components/SearchResult.vue";
// import { tab, info, base, detail } from "@/mock/data.js";

export default {
  name: "ViewWrap",

  components: {
    Search,
    SearchResult,
  },

  data: () => ({}),
};
</script>
