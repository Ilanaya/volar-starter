<template>
  <h1 class="test-reference"></h1>
</template>

<script lang="ts" setup>
</script>

<style>
.test-reference {}
</style>

<preview lang="md">
# This is preview page of HelloWorld.vue

## Props

| Props       | Description    |
| ----------- | -------------- |
| msg         | Title message  |

## Examples

<script setup>
const msgs = [
  'Hello Peter',
  'Hello John',
];
</script>

<template v-for="msg in msgs">
  <slot :msg="msg"></slot>
</template>

</preview>