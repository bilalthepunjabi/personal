<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "StackedShell",
  props: {},
  data() {
    return {};
  },
  methods: {},
});
</script>

<template>
<div class="min-h-full">
  <slot name="nav"></slot>
  <div class="py-10">
    <slot name="header"></slot>
    <main>
      <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
        <!-- Replace with your content -->
       <slot></slot>
        <!-- /End replace -->
      </div>
    </main>
  </div>
</div>
</template>