<template>
  <span
    @click="clickOnTag($event)"
    class="inline-flex items-center px-2 m-1 rounded-md text-xs font-medium bg-gray-300 text-gray-800 cursor-pointer"
  >
    {{ ticker.Symbol }}
  </span>
</template>

<script>
export default {
  name: "Tag",

  props: {
    ticker: null
  },

  methods: {
    clickOnTag(event) {
      this.$emit("clickOnTag", event.target.innerText);
    }
  }
};
</script>
