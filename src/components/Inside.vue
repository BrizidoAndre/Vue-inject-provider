<script setup>

</script>

<template>
  <header>
    <slot name="header">
      <p>
        Default Header
      </p>
    </slot>
  </header>
  <main>
    <slot>
      <h1>
        Default Value
      </h1>
    </slot>
  </main>
  <footer>
    <slot name="footer">
      <p>
        Default Footer
      </p>
    </slot>
  </footer>
</template>

<style scoped>

</style>