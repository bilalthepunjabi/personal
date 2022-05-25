<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from 'vue'

enum ContentEnum {
  NARROW = '',
  FULL = ''
}

export default defineComponent({
  name: "Container",
  props: {
    content: {
        type: String as PropType<ContentEnum>,
        required: false,
        default: () => (ContentEnum.FULL),
        validator: (content: ContentEnum) => {
            console.log('validating props : content => ',content);
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
          return this.content === ContentEnum.NARROW;
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
