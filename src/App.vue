<script lang="ts">
import { defineComponent, defineProps, reactive, ref } from "vue";
import type { PropType } from "vue";
import { RouterLink, RouterView } from "vue-router";

export default defineComponent({
  name: "App",
  components: {
    RouterView,
  },
  data() {
    return {};
  },
  methods: {},
});
</script>

<template>
  <RouterView />
</template>

<style>
@import "@/assets/base.css";
</style>
