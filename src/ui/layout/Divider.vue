<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "Divider",
  props: {
    text: {
      type: String,
    },
  },
  data() {
    return {};
  },
  methods: {},
});
</script>

<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="relative">
    <div class="absolute inset-0 flex items-center" aria-hidden="true">
      <div class="w-full border-t border-gray-300" />
    </div>
    <div class="relative flex justify-center">
      <span class="px-2 bg-white text-sm text-gray-500"> {{ text }} </span>
    </div>
  </div>
</template>
