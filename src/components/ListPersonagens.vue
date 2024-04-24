<script setup>
const personagem = defineProps(["name", "image"])
</script>

<template>
    <div class="col-md-3">
        <div class="card mb-3">
            <img :src="personagem.image" class="card-img-top" alt="...">
            <div class="card-body">
                <p class="card-title text-center">{{ personagem.name }}</p>
            </div>
        </div>
    </div>
</template>

<style>
p {
    font-size: 4vh;
}
.card-body {
    height: 19vh;
}
</style>