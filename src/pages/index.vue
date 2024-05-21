<script setup lang="ts">
import Hero from '@/components/Hero.vue'
import IconTheater from '@/components/icons/IconTheater.vue'
import IconMusic from '@/components/icons/IconMusic.vue'
import IconDanse from '@/components/icons/IconDanse.vue'
import Button from '@/components/Button.vue'
</script>
<template>
  <Hero
    title="Conservatoire Henri Dutilleux"
    subTitle="Conservatoire à Rayonnement Départemental du Grand Belfort"
    imgPath="./img/contrebasse.webp"
    imgAlt="Contrebasse"
  >
    <template #chapo>
      <nav class="font-serif flex-1">
        <ul class="grid grid-cols-3 gap-12">
          <li>
            <a class="flex flex-col items-center gap-4" href="#"><IconMusic /> Musique</a>
          </li>
          <li>
            <a class="flex flex-col items-center gap-4" href="#"><IconTheater /> Théâtre</a>
          </li>
          <li>
            <a class="flex flex-col items-center gap-4" href="#"><IconDanse /> Danse</a>
          </li>
        </ul>
      </nav>
    </template>
  </Hero>
  <section class="grille my-24 space-y-8 lg:grid-rows-2 lg:space-y-0">
    <img
      class="lg:col-span-7 lg:col-start-1 lg:row-span-2 lg:row-start-1"
      src="/img/crd-int-01.jpg"
      alt="Salle de musique du conservatoire"
    />
    <header
      class="space-y-8 bg-white lg:col-span-7 lg:col-start-6 lg:row-span-1 lg:row-start-1 lg:p-16"
    >
      <h2 class="text-xl italic leading-normal lg:text-3xl">
        Découvrez le Conservatoire, ses enseignements, ses équipes dans un nouveau lieu dédié à la
        culture artistique.
      </h2>
      <Button url="conservatoire" text="En savoir plus" />
    </header>

    <ul class="grid grid-cols-2 gap-12 lg:col-span-4 lg:col-start-9 lg:row-start-2">
      <li>
        <span class="block text-4xl text-pink lg:text-6xl">9</span>
        <span>sites</span>
      </li>
      <li>
        <span class="block text-4xl text-pink lg:text-6xl">84</span>
        <span>enseignants</span>
      </li>
      <li>
        <span class="block text-4xl text-pink lg:text-6xl">1500</span>
        <span>élèves</span>
      </li>
      <li>
        <span class="block text-4xl text-pink lg:text-6xl">50</span>
        <span>disciplines</span>
      </li>
    </ul>
  </section>
</template>
