<script setup lang="ts">
import Panel from "../ui/layout/Panel.vue"
</script>

<template>
  <main>
    <Panel>
      <template #header>
        <h1>Here might be a page title</h1>
      </template>
      
      <p>A paragraph for the main content.</p>
      <p>And another one.</p>

      <template #footer>
        <p>Here's some contact info</p>
      </template>
    </Panel>
  </main>
</template>
