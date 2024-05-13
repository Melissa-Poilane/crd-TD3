<script setup lang="ts">
import DuotoneImg from '@/components/DuotoneImg.vue'
import { formatDate } from '@/helper'
const props = defineProps<{
  id: number
  title: string
  date: string
  excerpt: string
  imgCardPath: string
  imgAlt?: string
}>()
</script>
<template>
  <article
    class="group col-span-6 grid grid-cols-[24px_1fr] grid-rows-[200px_48px_1fr] lg:grid-cols-[2fr_11fr] xl:col-span-4"
  >
    <DuotoneImg
      :imgPath="imgCardPath"
      :imgAlt="imgAlt"
      classPicture="col-start-1 row-start-1 col-span-2 row-span-2 group-hover:before:bg-black"
      classImg="group-hover:grayscale-0 group-hover:mix-blend-normal"
    />
    <h3 class="z-[1] col-start-2 row-start-1 my-6 mr-4 text-white text-3xl self-end">
      <a href="#">{{ title }}</a>
    </h3>
    <div class="z-[2] col-span-1 col-start-2 row-span-2 row-start-2 bg-white p-6 space-y-4">
      <p class="uppercase">{{ formatDate(date) }}</p>
      <p>{{ excerpt }}</p>
      <a class="inline-block border-b-2 border-black uppercase" href="#">Plus d'info</a>
    </div>
  </article>
</template>
