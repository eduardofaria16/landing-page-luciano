<template>
  <footer style="background-color: #303829; color: #fff; padding: 20px 0; text-align: center;">
    <p style="margin: 5px 0; font-size: 16px; font-weight: bold;">Luciano Tarso</p>
    <p style="margin: 5px 0; font-size: 14px;">Psicólogo Clínico - CRP-04 / 82152</p>
    <p style="margin: 5px 0; font-size: 14px;">Uberlândia, MG</p>
    <p style="margin: 5px 0; font-size: 14px;">tarsoluciano@gmail.com | (34) 99687-7462</p>
    <p style="margin: 10px 0 0; font-size: 12px; color: #ccc;">
      &copy; {{ currentYear }} Luciano Tarso - Todos os direitos reservados.
    </p>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>
