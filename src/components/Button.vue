<script setup lang="ts">
import ArrowIcon from '@/components/icons/IconArrow.vue'
const props = withDefaults(
  defineProps<{
    variant?: 'default' | 'dark' | 'outlined'
    url: string
    text: string
  }>(),
  { variant: 'default' }
)

const variantClass = {
  default: 'border border-pink hover:shadow-[inset_0_0_0_8px_#feaa9b]',
  dark: 'bg-black text-white',
  outlined: 'text-white border border-white hover:shadow-[inset_0_0_0_8px_white]'
}
</script>
<template>
  <RouterLink
    class="inline-flex items-center gap-4 px-6 py-4 text-xs font-bold uppercase tracking-wide transition duration-300 ease-in-out lg:px-8 lg:py-6 lg:text-sm"
    :class="variantClass[props.variant]"
    :to="`${url}`"
  >
    <ArrowIcon :class="$props.variant === 'default' ? 'stroke-black' : 'stroke-white'" />
    {{ text }}
  </RouterLink>
</template>
