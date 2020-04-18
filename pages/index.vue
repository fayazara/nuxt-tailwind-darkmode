<template>
  <div class="bg-gray-100 dark:bg-gray-800 transition-all duration-300 min-h-screen">
    <navbar />
    <div class="container mx-auto pt-24 p-4">
      <stats :stats="data.statewise[0]" />
      <cases :states="data.statewise" />
    </div>
  </div>
</template>

<script>
import navbar from "~/components/navbar";
import stats from "~/components/stats";
import cases from "~/components/cases";
export default {
  components: {
    stats,
    cases,
    navbar
  },
  async asyncData({ $axios }) {
    const { data } = await $axios.get(`https://api.covid19india.org/data.json`);
    return { data };
  }
};
</script>
