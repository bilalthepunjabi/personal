<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "List",
  props: {},
  data() {
    return {
      items: [],
    };
  },
  methods: {},
});
</script>

<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="bg-white shadow overflow-hidden rounded-md">
    <ul role="list" class="divide-y divide-gray-200 space-y-3">
      <slot></slot>
    </ul>
  </div>
</template>
