<template>
  <div class="min-h-full flex items-center justify-center my-4 mx-12">
    <div class="w-full mx-3 border-2 p-4">
      <p class="font-medium mb-4">Transactions</p>
      <SearchBar class="my-4" />
      <TableData class="my-4" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'TransactionsPage'
})
</script>
