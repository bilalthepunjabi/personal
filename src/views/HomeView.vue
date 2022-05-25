<script setup lang="ts">
import List from "../ui/layouts/List.vue";
import Item from "../ui/layouts/Item.vue";
import Divider from "../ui/layouts/Divider.vue";
import StackedShell from "../ui/shells/stacked/StackedShell.vue";
import NavBar from "../ui/navigations/NavBar.vue";
</script>

<template>
  <StackedShell>
    <template #nav>
      <NavBar/>
    </template>
    <List>
      <Item> 1 </Item>
      <Item> 2 </Item>
      <Item> 3 </Item>
    </List>
  </StackedShell>
</template>
