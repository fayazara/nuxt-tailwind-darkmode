<template>
  <div
    class="bg-gray-100 dark:bg-black transition-all duration-300 min-h-screen"
  >
    <navbar />
    <div class="container mx-auto pt-24 p-4" v-if="source">
      <stats :stats="source.statewise[0]" />
      <cases :states="source.statewise" />
      <p class="text-center">
        <a
          class=" text-center text-gray-700 dark:text-white my-8"
          href="https://www.covid19india.org/"
          >Data Source</a
        >
      </p>
    </div>
  </div>
</template>

<script>
import navbar from "~/components/navbar";
import stats from "~/components/stats";
import cases from "~/components/cases";
export default {
  data() {
    return {
      source: null
    };
  },
  components: {
    stats,
    cases,
    navbar
  },
  async mounted() {
    const { data } = await this.$axios.get(
      `https://api.covid19india.org/data.json`
    );
    this.source = data;
  }
};
</script>
