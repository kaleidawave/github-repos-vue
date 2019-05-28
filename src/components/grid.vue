<template>
  <div>
    <table>
      <tr>
        <th v-for="label in header" v-bind:key="label.id" v-html="label"></th>
      </tr>
      <Row v-for="item in content" v-bind:content="item" v-bind:key="item.id"></Row>
    </table>
  </div>
</template>

<script>
import Row from "./row.vue";

export default {
  name: "Grid",
  components: { Row },
  props: ["header", "content"]
};
</script>

<style src="./grid.css"></style>
