<template>
  <div class="py-4">
    <div class="-mx-4 sm:-mx-8 px-4 sm:px-8 py-4 overflow-x-auto">
      <div class="inline-block min-w-full shadow rounded-lg overflow-hidden">
        <table class="min-w-full leading-normal">
          <thead>
            <tr class="text-gray-600 dark:text-white">
              <th
                class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100  dark:border-gray-500 dark:bg-gray-600 text-left text-xs font-semibold uppercase tracking-wider"
              >
                State
              </th>
              <th
                class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100  dark:border-gray-500 dark:bg-gray-600 text-left text-xs font-semibold uppercase tracking-wider"
              >
                Confirmed
              </th>
              <th
                class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100  dark:border-gray-500 dark:bg-gray-600 text-left text-xs font-semibold uppercase tracking-wider"
              >
                Active
              </th>
              <th
                class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100  dark:border-gray-500 dark:bg-gray-600 text-left text-xs font-semibold uppercase tracking-wider"
              >
                Recovered
              </th>
              <th
                class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100  dark:border-gray-500 dark:bg-gray-600 text-left text-xs font-semibold uppercase tracking-wider"
              >
                Deceased
              </th>
            </tr>
          </thead>
          <tbody class="dark:text-white transition-all">
            <tr v-for="(state, i) in states" :key="i">
              <td class="px-5 py-5 border-b border-gray-200 dark:border-gray-500 bg-white dark:bg-gray-700 text-sm">
                <p>{{state.state}}</p>
              </td>
              <td class="px-5 py-5 border-b border-gray-200 dark:border-gray-500 bg-white dark:bg-gray-700 text-sm">
                <p>{{state.confirmed}}</p>
              </td>
              <td class="px-5 py-5 border-b border-gray-200 dark:border-gray-500 bg-white dark:bg-gray-700 text-sm">
                <p>{{state.active}}</p>
              </td>
              <td class="px-5 py-5 border-b border-gray-200 dark:border-gray-500 bg-white dark:bg-gray-700 text-sm">
                <p>{{state.recovered}}</p>
              </td>
              <td class="px-5 py-5 border-b border-gray-200 dark:border-gray-500 bg-white dark:bg-gray-700 text-sm">
                <p>{{state.deaths}}</p>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["states"]
};
</script>

<style></style>
