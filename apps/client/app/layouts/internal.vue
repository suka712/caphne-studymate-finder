<template>
  <div class="dark min-h-screen bg-background text-foreground">
    <ProgressBar />
    <main class="mx-auto max-w-7xl">
      <slot />
    </main>
    <ProgressControl />
  </div>
</template>
