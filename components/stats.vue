<template>
  <div
    class="grid grid-cols-2 gap-2 sm:grid-cols-2 md:grid-cols-4 lg:grid-cols-4 xl:grid-cols-4"
  >
    <div
      class="bg-red-500 dark:bg-gray-900 transition-all duration-300 text-white dark:text-red-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.confirmed }}</p>
      <p>Confirmed</p>
    </div>
    <div
      class="bg-blue-500 dark:bg-gray-900 transition-all duration-300 text-white dark:text-blue-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.active }}</p>
      <p>Active</p>
    </div>
    <div
      class="bg-green-500 dark:bg-gray-900 transition-all duration-300 text-white dark:text-green-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.recovered }}</p>
      <p>Recovered</p>
    </div>
    <div
      class="bg-gray-600 dark:bg-gray-900 transition-all duration text-white  px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.deaths }}</p>
      <p>Deceased</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["stats"]
};
</script>

<style></style>
