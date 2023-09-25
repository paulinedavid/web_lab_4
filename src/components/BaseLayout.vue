<template>
    <BaseHeader />
    <slot></slot>
    <BaseFooter />
</template>

<script setup>
import BaseHeader from './BaseHeader.vue'
import BaseFooter from './BaseFooter.vue'
</script>

<style>
:root {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
