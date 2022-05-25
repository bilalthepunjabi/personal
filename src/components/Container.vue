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
          narrow : false
        }),
        validator: (content) => {
            console.log('validating props : constrained => ',content, typeof(content));
            return true;
        }
    },
  },
  data() {
    return {
    };
  },
  methods: {},
});
</script>

<template>
<div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
  <slot v-if="!constrained.narrow"></slot>
  <div class="max-w-3xl mx-auto" v-if="constrained.narrow">
    <slot v-if="constrained.narrow"></slot>
  </div>
</div>
</template>
