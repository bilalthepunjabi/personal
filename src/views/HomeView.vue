<script setup lang="ts">
import List from "../ui/layout/List.vue";
import Item from "../ui/layout/Item.vue";
import Divider from "../ui/layout/Divider.vue";
import StackedOverlap from "../ui/shells/stacked/StackedOverlap.vue";
</script>

<template>
  <StackedOverlap>
    <template #nav>
      Navs
    </template>
    <template #header>
      Dashboard
    </template>
    <List>
      <Item> 1 </Item>
      <Divider text="continue" />
      <Item> 2 </Item>
      <Item> 3 </Item>
    </List>
  </StackedOverlap>
</template>
