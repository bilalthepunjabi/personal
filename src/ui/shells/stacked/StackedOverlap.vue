<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "StackedOverlap",
  props: {},
  data() {
    return {};
  },
  methods: {},
});
</script>
<template>
<div class="min-h-full">
  <div class="bg-gray-800 pb-32">
    <slot name="nav"></slot>
    <slot name="header"></slot>
  </div>

  <main class="-mt-32">
    <div class="max-w-7xl mx-auto pb-12 px-4 sm:px-6 lg:px-8">
      <!-- Replace with your content -->
      <slot></slot>
      <!-- /End replace -->
    </div>
  </main>
</div>
</template>