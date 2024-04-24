<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';

let personagem = reactive(ref());

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character/?limit=50&offset=0")
  .then(response => response.json())
  .then(response => {
    personagem.value = response.results;
    console.log(personagem);
  });
});
</script>
<template>
  <main>
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-12 col-md-12" >
          
            <div class="card-body row" >
              <ListPersonagens
              v-for="personagem in personagem"
              :key="personagem.id"
              :name="personagem.name"
              :image="personagem.image"
            ></ListPersonagens>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
