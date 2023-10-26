<script setup></script>

<template>
  <div class="container">
    <h1 class="title">Stack:</h1>
    <ul>
      <li>Vue</li>
      <li>Axios</li>
      <li>Sweetalert2</li>
      <li>Vite</li>
    </ul>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 50vh;
}

.title {
  font-size: 32px;
}

.title ul li {
  margin-top: 10px;
  font-size: 20px;
  list-style: square;
}
</style>
