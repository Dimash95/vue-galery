<script setup>
import { computed, onMounted, ref, watch } from "vue";
import axios from "axios";
import Swal from "sweetalert2";

const getPics = async () => {
  const response = await axios.get(
    "https://653928ffe3b530c8d9e8065d.mockapi.io/pictures"
  );
  pictures.value = response.data;
};

onMounted(() => getPics());

const pictures = ref([]);

const openModal = (url, author) => {
  Swal.fire({
    imageUrl: url,
    imageAlt: "image",
    imageHeight: 600,
  });
};

const searchedValue = ref("");

const filterPicture = computed(() => {
  return pictures.value.filter((filtered) => {
    return filtered.name
      .toLowerCase()
      .includes(searchedValue.value.toLocaleLowerCase());
  });
});

watch(searchedValue, () => getPics());
</script>

<template>
  <div class="container">
    <input
      class="input"
      type="text"
      placeholder="Поиск..."
      v-model="searchedValue"
    />
    <div class="cards">
      <div class="card" v-for="picture in filterPicture" :key="picture.id">
        <img
          @click="openModal(picture.url, picture.author)"
          :src="picture.url"
          alt="pic"
        />
        <p class="name">{{ picture.name }}</p>
        <p>{{ picture.author }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}

.input {
  max-width: 500px;
  width: 100%;
  margin: 0 auto;
  margin-top: 20px;
  padding: 5px;
  font-size: 16px;
}

.cards {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
  max-width: 1220px;
  width: 100%;
  margin: 0 auto;
  padding: 20px 0;
}

.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 300px;
  height: 440px;
  margin: 0 auto;
  border: 1px solid black;
}

.card img {
  width: 300px;
  height: 340px;
  cursor: pointer;
}

.card p {
  margin-top: 20px;
  text-align: center;
}

.name {
  font-weight: bold;
}
</style>
