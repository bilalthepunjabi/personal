<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  name: "Container",
  props: {
    constrained: {
      type: Object,
      required: false,
      default: () => ({
        narrow: false,
      }),
      validator: (payload) => {
        return true;
      },
    },
    padding: {
      type: String,
      required: false,
      default: "",
      validator: (payload) => {
        return typeof payload === "string";
      },
    },
    responsive: {
      type: Boolean,
      required: false,
      default: true,
      validator: (payload) => {
        return typeof payload === "boolean";
      },
    },
  },
  data() {
    return {};
  },
  methods: {},
});
</script>

<template>
  <div
    :class="!responsive ? 'max-w-7xl ' + padding : 'container'"
    class="mx-auto sm:px-6 lg:px-8"
  >
    <slot v-if="!constrained?.narrow"></slot>
    <div class="max-w-3xl mx-auto" v-if="constrained?.narrow">
      <slot v-if="constrained?.narrow"></slot>
    </div>
  </div>
</template>
