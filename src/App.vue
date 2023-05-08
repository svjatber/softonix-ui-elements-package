<script setup lang="ts">
import SButton from './components/SButton.vue';
</script>

<template>
  <div class="flex">
    <SButton type="primary">Primary</SButton>
    <SButton type="primary" disabled>Primary(disaled)</SButton>
    <SButton type="secondary" >Secondary</SButton>
    <SButton type="secondary" disabled>Secondary(disabled)</SButton>
    <SButton type="specific">Specific</SButton>
    <SButton type="specific" disabled>Specific(disabled)</SButton>
  </div>
</template>

<style>
.flex {
  display: flex;
  gap: 5px;
  flex-wrap: wrap;
}
</style>
