<template>
  <div>
    <table v-if="filteredData.length">
      <!-- ... Tablo başlıkları ... -->
      <tbody>
        <tr v-for="entry in filteredData" :key="entry">
          <td v-for="key in columns" :key="key">
            {{ entry[key] }}
          </td>
        </tr>
      </tbody>
    </table>
    <p v-else>No matches found.</p>
  </div>
</template>

<script setup>
import { ref, computed, defineProps } from 'vue'

const props = defineProps({
  data: Array,
  columns: Array,
  filterKey: String
})

// ... Diğer kodlar ...
</script>

<style>
/* ... Stil kuralları ... */
</style>
