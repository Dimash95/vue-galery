<script setup></script>

<template>
  <div class="container">
    <div class="content">
      <h1 class="logo">Galery</h1>
      <div class="made">Made by Dimash</div>
      <ul>
        <li>
          <a href="https://github.com/Dimash95" target="blank"
            ><img
              src="../assets/svg/github.svg"
              alt="github"
              width="40"
              height="40"
          /></a>
        </li>
        <li>
          <a
            href="https://www.linkedin.com/in/dinmukhamed-amirov-4b520726b/"
            target="blank"
            ><img
              src="../assets/svg/linkedin.svg"
              alt="linkedin"
              width="40"
              height="40"
          /></a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  background-color: lightblue;
  flex: 0 0 auto;
}

.logo {
  font-size: 32px;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100px;
  max-width: 1100px;
  width: 90%;
  margin: 0 auto;
}

.made {
  font-size: 20px;
}

ul {
  display: flex;
  gap: 20px;
}

li {
  list-style: none;
}
</style>
