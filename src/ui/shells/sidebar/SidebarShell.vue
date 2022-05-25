<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "SidebarShell",
  props: {},
  data() {
    return {};
  },
  methods: {},
});
</script>
<template>
    <!--
  This example requires Tailwind CSS v2.0+ 
  
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->
<!--
  This example requires updating your template:

  ```
  <html class="h-full bg-gray-100">
  <body class="h-full">
  ```
-->
<div>
  <!-- Off-canvas menu for mobile, show/hide based on off-canvas menu state. -->
  <slot name="mobile_nav"></slot>
  <!-- Static sidebar for desktop -->
  <slot name="sidebar"></slot>
  <div class="md:pl-64 flex flex-col flex-1">
    <slot name="nav"></slot>
    <main>
      <div class="py-6">
        <slot name="header"></slot>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 md:px-8">
          <!-- Replace with your content -->
            <slot></slot>
          <!-- /End replace -->
        </div>
      </div>
    </main>
  </div>
</div>

</template>