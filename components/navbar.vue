<template>
  <nav class="py-4 bg-white dark:bg-gray-900 border-b border-gray-300 dark:border-gray-700 text-gray-600 dark:text-white fixed w-full transition-all duration-300">
    <div class="container mx-auto flex justify-between px-4 items-center">
      <p class="font-semibold uppercase tracking-wider">
        Covid19 India
      </p>
      <button @click="toggle" class="">
        <svg
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          viewBox="0 0 24 24"
          class="w-8 h-8"
        >
          <path
            d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"
          ></path>
        </svg>
      </button>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    toggle() {
      this.$colorMode.preference =
        this.$colorMode.value == "light" ? "dark" : "light";
    }
  }
};
</script>
