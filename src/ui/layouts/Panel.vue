<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "Panel",
  props: {
    
  },
  data() {
    return {};
  },
  methods: {},
});
</script>

<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="bg-white overflow-hidden shadow rounded-lg divide-y divide-gray-200">
    <div class="px-4 py-5 sm:px-6">
      <!-- Content goes here -->
      <!-- We use less vertical padding on card headers on desktop than on body sections -->
      <slot name="header"></slot>
    </div>
    <div class="px-4 py-5 sm:p-6">
      <!-- Content goes here -->
      <slot></slot>
    </div>
    <div class="px-4 py-4 sm:px-6">
      <!-- Content goes here -->
      <!-- We use less vertical padding on card footers at all sizes than on headers or body sections -->
      <slot name="footer"></slot>
    </div>
  </div>
</template>