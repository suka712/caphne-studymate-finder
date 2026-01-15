<script setup lang="ts">
definePageMeta({ layout: "internal" })
</script>

<template>
  <div class="flex flex-col justify-center items-center h-screen gap-6">
    <h1>Your gender is...</h1>
    <div class="flex flex-col gap-2 justify-center">
      <div class="flex justify-center gap-2">
        <Button class="hover:px-6">Male</Button>
        <Button class="hover:px-6">Female</Button>
      </div>
      <Button variant="outline" class="hover:px-6">Something else</Button>
    </div>
  </div>
</template>