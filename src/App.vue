<template>
<div class="app">
  <nav>
    <RouterLink to="/">Home</RouterLink> |
    <RouterLink to="/about">About</RouterLink>
  </nav>

  <RouterView />
</div>
</template>

<style>
.app {
  text-align: center;
  font-size: 3rem;
}
</style>