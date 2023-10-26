<script setup></script>

<template>
  <div class="container">
    <div class="content">
      <h1 class="logo">Galery</h1>
      <ul>
        <li><router-link to="/" class="link">Главная</router-link></li>
        <li><router-link to="/about" class="link">О нас</router-link></li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 100%;
  background-color: lightblue;
}

.logo {
  font-size: 32px;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  max-width: 1100px;
  width: 90%;
  margin: 0 auto;
  padding: 10px;
}

.content ul {
  display: flex;
  gap: 20px;
}

.content ul li {
  font-size: 18px;
  list-style: none;
}

.link {
  color: black;
  text-decoration: none;
  transition: 0.4s;
}

.link:hover {
  text-decoration: underline;
}
</style>
