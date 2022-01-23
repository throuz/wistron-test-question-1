<template>
  <v-simple-table>
    <tbody>
      <tr v-for="(item, i) in content" :key="i">
        <td>{{ item.key }}</td>
        <td v-if="Array.isArray(item.value)" class="pr-0">
          <v-simple-table>
            <tbody>
              <tr v-for="(obj, j) in item.value" :key="j">
                <td>{{ obj["State Name"] }}</td>
                <td>{{ obj["State Value"] }}</td>
              </tr>
            </tbody>
          </v-simple-table>
        </td>
        <td v-else>
          {{ item.value }}
          <v-btn v-if="item.btn" class="ml-4" small color="secondary">{{
            item.btn
          }}</v-btn>
        </td>
      </tr>
    </tbody>
  </v-simple-table>
</template>

<script>
export default {
  name: "SearchResult",

  props: {
    content: {
      type: Array,
      required: true,
    },
  },
};
</script>
