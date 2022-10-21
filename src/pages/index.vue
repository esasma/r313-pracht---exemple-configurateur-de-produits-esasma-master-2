<script setup lang="ts">
import BasketProfil from "../components/BasketProfil.vue";
import type { Basket } from "../types";
const exemple: Basket = [{
  semelle: "#FF0000",
  empeigne: "#FFFFFF",
  pointe: "#FFFFFF",
  oeillet: "#FFFFFF",
  bande: "#00FF00",
  languette: "#FFFFFF",
  lacet: "#00FF00",
  trimestre: "#FFFFFF",
},
{
  semelle: "#00ff00",
  empeigne: "#F45FFF",
  pointe: "#FF95FF",
  oeillet: "#Ca25ff",
  bande: "#00FF00",
  languette: "#FFFFFF",
  lacet: "#00FF00",
  trimestre: "#FFFFFF",
}];
</script>
<template>
  <section>
    <h1 class="text-2xl">Exemples de Baskets</h1>
    <div class="flex flex-wrap gap-2">
      <div class="w-64">
        <RouterLink v-for="ex in exemple" :key="exemple.id"
          :to="{
            name: 'basket-exemple-data',
            params: { data: JSON.stringify(ex) },
          }"
        >
          <BasketProfil class="w-64" v-bind="ex" />
        </RouterLink>
      </div>
    </div>
  </section>
</template>