<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
    </nav>
  </header>
  <div></div>
  <RouterView />
</template>
<script></script>
<style scoped>
header {
  position: sticky;
  height: 50px;
  padding: 10px;
}
</style>
