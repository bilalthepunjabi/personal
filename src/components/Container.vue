<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from 'vue'
import { ConstrainedEnum } from './types/Container';

export default defineComponent({
  name: "Container",
  props: {
    constrained: {
        type: String as PropType<ConstrainedEnum>,
        required: false,
        default: () => (ConstrainedEnum.FULL),
        validator: (content: ConstrainedEnum) => {
            console.log('validating props : content => ',content, typeof(content));
            return true;
        }
    },
  },
  data() {
    return {
    };
  },
  methods: {
      narrow(){
          return this.constrained === ConstrainedEnum.NARROW;
      }
  },
});
</script>

<template>
<div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
  <slot v-if="!narrow()"></slot>
  <div class="max-w-3xl mx-auto" v-if="narrow()">
    <slot v-if="narrow()"></slot>
  </div>
</div>
</template>
