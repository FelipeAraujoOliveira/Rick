<script setup>
const personagem = defineProps(["name", "image", "status", "species", "gender", "location", "episode"])

</script>

<template>
    <div class="col-md-3">
        <div class="card mb-3">
            <div class="card-body">
                <p class="card-title text-center"> <b>NAME: </b>{{ personagem.name }}</p>
                <img style="border-radius: 1vh;" :src="personagem.image" class="card-img-top" alt="">
                <p class="card-title text-center"><b>STATUS: </b>{{ personagem.status }}</p>
                <p class="card-title text-center"><b>SPECIES: </b>{{ personagem.species }}</p>
                <p class="card-title text-center"><b>GENDER: </b>{{ personagem.gender }}</p>
                <p class="card-title text-center"><b>LOCATION: </b>{{ personagem.location }}</p>
                <p class="card-title text-center"><b>EPISODES: </b>{{ personagem.episode }}</p>
            </div>
            
        </div>
    </div>
</template>

<style>
p {
    font-size: 2.3vh;
}
.card-body {
    height: 65vh;
}
</style>

<style scoped>
.card {
  border: 1px solid #ccc;
}
</style>
