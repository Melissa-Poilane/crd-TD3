<script setup lang="ts">
import Hero from '@/components/Hero.vue'
import IconTheater from '@/components/icons/IconTheater.vue'
import IconMusic from '@/components/icons/IconMusic.vue'
import IconDanse from '@/components/icons/IconDanse.vue'
</script>
<template>
  <Hero
    title="Conservatoire Henri Dutilleux"
    subTitle="Conservatoire à Rayonnement Départemental du Grand Belfort"
    imgPath="./img/contrebasse.webp"
    imgAlt="Contrebasse"
  >
    <template #chapo>
      <nav>
        <ul>
          <li>
            <a href="#"><IconMusic /> Musique</a>
          </li>
          <li>
            <a href="#"><IconTheater /> Théâtre</a>
          </li>
          <li>
            <a href="#"><IconDanse /> Danse</a>
          </li>
        </ul>
      </nav>
    </template>
  </Hero>
</template>
