<script setup lang="ts">
import DuotoneImg from '@/components/Duotoneimg.vue'

defineProps<{
  title: string
  subTitle?: string
  imgPath: string
  imgAlt: string
}>()
</script>
<template>
  <div class="grille grid h-dvh grid-rows-[4fr_1fr] lg:grid-rows-[3fr_1fr]">
    <div class="self-end my-12 space-y-8 text-white lg:col-span-9">
      <h1>{{ title }}</h1>
      <h2 class="font-sans text-sm font-bold uppercase" v-if="subTitle">{{ subTitle }}</h2>
    </div>

    <div
      class="bg-white -mx-6 px-6 flex items-center lg:col-span-9 lg:mx-0 lg:pl-0 lg:relative lg:before:absolute lg:before:top-0 lg:before:h-full lg:before:w-full lg:before:-ml-[100%] lg:before:bg-white"
    >
      <slot name="chapo"></slot>
    </div>
    <DuotoneImg
      classPicture="!absolute inset-0 object-cover z-[-1]"
      :imgPath="imgPath"
      :imgAlt="imgAlt"
    />
  </div>
</template>
