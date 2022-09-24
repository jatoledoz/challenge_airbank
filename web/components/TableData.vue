<template>
  <div class="mt-2">
    <div
      class="grid grid-cols-12 gap-6 py-4 px-2 border-t-2 border-b-2 text-sm font-thin"
    >
      <p class="col-span-7">Reference</p>
      <p class="col-span-3">Category</p>
      <p>Date</p>
      <p class="flex align-middle self-end justify-end">Amount</p>
    </div>
    <div
      v-for="transaction in transactions"
      :key="transaction"
      class="grid grid-cols-12 gap-6 py-4 px-2 text-sm font-light border-b"
    >
      <p v-if="transaction.reference.length > 0" class="col-span-7">
        {{ transaction.reference }}
      </p>
      <p v-else class="col-span-7 font-thin">No reference provided</p>

      <div class="col-span-3">
        <p>
          {{ transaction.category }}
        </p>
      </div>
      <p>
        {{ transaction.date }}
      </p>
      <p class="flex align-middle self-end justify-end">
        <span v-if="transaction.transactionType == 'outcome'">-</span>
        {{ transaction.amount }}
        <span class="font-thin ml-1">{{ transaction.currency }}</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      transactions: [
        {
          reference: 'Reconcialitory blablabla',
          category: 'Advertising',
          date: '14/03/22',
          amount: 438.0,
          currency: 'GBP',
          transactionType: 'income'
        },
        {
          reference: '',
          category: 'Vendors',
          date: '30/03/22',
          amount: 30.0,
          currency: 'EUR',
          transactionType: 'outcome'
        },
        {
          reference: 'Product sale',
          category: 'Sales and Marketing',
          date: '05/04/22',
          amount: 3000.0,
          currency: 'USD',
          transactionType: 'income'
        }
      ]
    }
  }
}
</script>
