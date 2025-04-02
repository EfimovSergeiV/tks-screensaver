<template>
  <div class="bg-fixed bg-cover bg-[url('tks-logo.png')] dark:bg-[url('tks-logo.png')] min-h-screen">
    <div class="fixed inset-0 bg-gradient-to-r from-black/25 via-transparent to-black/25 pointer-events-none">
      <div class="fixed inset-0 bg-gradient-to-b from-black/25 via-transparent to-black/25 pointer-events-none">

        <slot />

      </div>
    </div>
  </div>
</template>