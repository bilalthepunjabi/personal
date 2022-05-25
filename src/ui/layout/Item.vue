<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "Item",
  props: {},
  data() {
    return {};
  },
  methods: {},
});
</script>

<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <li class="px-6 py-4">
    <slot></slot>
  </li>
</template>
