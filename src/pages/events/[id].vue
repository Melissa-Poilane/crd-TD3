<script setup lang="ts">
import { events } from '@/data'
import { useRoute } from 'vue-router/auto'
import DuotoneImg from '@/components/DuotoneImg.vue'
import { formatDate } from '@/helper'

const route = useRoute('/events/[id]')
const event = events.find((event) => event.id === Number(route.params.id))
const props = defineProps<{ id: string }>()
</script>
<template>
  <div v-if="event">
    <div class="grille relative pt-28">
      <DuotoneImg :imgPath="event.imgPath" :imgAlt="event.imgAlt" classPicture="lg:col-span-5" />
      <header class="lg:col-span-6 lg:col-start-7">
        <h1 class="my-12">{{ event.title }}</h1>
        <ul class="divide-y *:grid *:grid-cols-4 *:items-center *:py-4">
          <li>
            <span class="col-span-1 text-sm font-bold uppercase">Date</span>
            <span class="col-span-3">{{ formatDate(event.date) }}</span>
          </li>
          <li>
            <span class="col-span-1 text-sm font-bold uppercase">Lieux</span>
            <span class="col-span-3">{{ event.lieu }}</span>
          </li>
          <li>
            <span class="col-span-1 text-sm font-bold uppercase">Catégorie</span>
            <span class="col-span-3">{{ event.categorie }}</span>
          </li>
        </ul>
      </header>
    </div>
    <p
      class="my-12 px-6 text-2xl leading-normal lg:mx-auto lg:max-w-4xl lg:text-3xl lg:leading-relaxed"
    >
      {{ event?.excerpt }}
    </p>
    <div class="my-12 space-y-3 px-6 lg:mx-auto lg:max-w-2xl" v-html="event?.description"></div>
  </div>
  <div v-else>
    <h1>Pas d'événement correspondant</h1>
  </div>
</template>
