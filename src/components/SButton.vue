<template>
  <button v-bind="$attrs" :class="['s-button', baseClass]" type="button">
    <slot />
  </button>
</template>

<script setup lang="ts">
import { computed } from 'vue';
import { ESButtonType } from '../types';

type TButton = `${ESButtonType}`
const props = withDefaults(
  defineProps<{ type: TButton }>(), 
  { type: ESButtonType.PRIMARY }
)
const variantClass = {
  [ESButtonType.PRIMARY]: 's-button-primary',
  [ESButtonType.SECONDARY]: 's-button-secondary',
  [ESButtonType.SPECIFIC]: 's-button-specific',
}

const baseClass = computed(() => variantClass[props.type])
</script>