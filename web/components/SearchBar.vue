<template>
  <div>
    <div class="grid grid-cols-8 gap-4 font-extralight">
      <p class="col-span-4">Search</p>
      <p>Bank</p>
      <p>Account</p>
      <p>Starting month</p>
      <p>Ending month</p>
    </div>
    <div class="grid grid-cols-8 gap-4">
      <input
        type="text"
        placeholder="Search by bank, account, reference, category, date, amount, currency..."
        class="col-span-4"
      />
      <select id="banks" name="banks">
        <option value="">No filter applied</option>
      </select>
      <select id="accounts" name="accounts">
        <option value="">No filter applied</option>
      </select>
      <input id="startingMonth" type="date" name="startingMonth" />
      <input id="endingMonth" type="date" name="endingMonth" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style></style>
