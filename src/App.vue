<script lang="ts">
import { defineComponent, defineProps, reactive, ref } from "vue";
import type { PropType } from 'vue'

import { RouterLink, RouterView } from 'vue-router'
import Container from './components/Container.vue'
import { ConstrainedEnum } from './components/types/Container';

interface state {
  constrained: ConstrainedEnum
}

export default defineComponent({
  name: "App",
  components:{
    Container,
    RouterView
  },
  setup () {
    const state = reactive<state>({
      constrained: ref(ConstrainedEnum.NARROW)
    });
    return { state }
  },
  methods: {

  },
});
</script>

<template>
  <Container :constrained="constrained">
    <RouterView/>
  </Container>
</template>

<style>
@import '@/assets/base.css';
</style>
