<script setup lang="ts">
import FormBasket from "../../../components/FormBasket.vue";
defineProps<{
  data: string;
}>();
</script>


<template>
  <FormBasket :data="JSON.parse(data)" />
</template>