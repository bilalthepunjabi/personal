<script lang="ts">
import { defineComponent, defineProps, reactive, ref } from "vue";
import type { PropType } from 'vue'

import { RouterLink, RouterView } from 'vue-router'
import Container from './components/Container.vue'

interface state {
  constrained: Object
}

export default defineComponent({
  name: "App",
  components:{
    Container,
    RouterView
  },
  data(){
    return {
      constrained : {
        narrow : false
      }
    }
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
