<script setup>
import {ref} from 'vue'
</script>

<template>
<nav class="navbar navbar-expand-lg bg-body-tertiary" data-bs-theme="dark">
  <div class="container-fluid">
    <router-link class="navbar-brand" to="/"><img class="logo" src="/src/assets/Rick_and_Morty.svg.png" alt=""></router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <router-link class="nav-link" arial-current="page" to="/">Inicio</router-link>
        <router-link class="nav-link" arial-current="page" to="/about">Sobre</router-link>
      </div>
    </div>
  </div>
</nav>

<div class="mais">
  <router-view></router-view>
</div>

</template>

<style>
body {
  background-color: rgb(29, 29, 29);
  font-family:Verdana, Geneva, Tahoma, sans-serif;
}
.logo{
  width: 20vh;
}

</style>    