<script setup lang="ts">
import DuotoneImg from '@/components/DuotoneImg.vue'

defineProps<{
  title: string
  subTitle?: string
  imgPath: string
  imgAlt: string
}>()
</script>
<template>
  <div>
    <div>
      <h1>{{ title }}</h1>
      <h2 v-if="subTitle">{{ subTitle }}</h2>
    </div>

    <div><slot name="chapo"></slot></div>
    <DuotoneImg :imgPath="imgPath" :imgAlt="imgAlt" />
  </div>
</template>
