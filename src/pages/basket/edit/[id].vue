<script setup lang="ts">
import FormBasket from "../../../components/FormBasket.vue";
defineProps<{
  id: string;
}>();
</script>

<template>
  <FormBasket :id="id" />
</template>