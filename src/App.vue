<script lang="ts">
import { defineComponent, defineProps, reactive, ref } from "vue";
import type { PropType } from "vue";
import { RouterLink, RouterView } from "vue-router";

import Container from "./components/Container.vue";

export default defineComponent({
  name: "App",
  components: {
    Container,
    RouterView,
  },
  data() {
    return {};
  },
  methods: {},
});
</script>

<template>
  <Container>
    <RouterView />
  </Container>
</template>

<style>
@import "@/assets/base.css";
</style>
