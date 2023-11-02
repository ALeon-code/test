<script setup>
import {ref, reactive, computed} from 'vue';

const props = defineProps({
  values: {
    type: Array,
    required: true,
  }
})
</script>

<template>
  <tr class="table-row">
    <td v-for="(value, index) in values" :key="index">
      {{ value }}
    </td>
  </tr>
</template>

<style lang="scss" rel="stylesheet/scss" scoped>
tr {
  background-color: white;
  border-radius: 4px;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.08);
}
td {
  padding: 8px;
}
</style>
