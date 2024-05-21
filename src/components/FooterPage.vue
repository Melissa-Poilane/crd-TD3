<script setup lang="ts">
import FacebookIcon from '@/components/icons/IconFacebook.vue'
import TwitterIcon from '@/components/icons/IconTwitter.vue'
import YoutubeIcon from '@/components/icons/IconYoutube.vue'
import InstagramIcon from '@/components/icons/IconInstagram.vue'
import LogoGBIcon from '@/components/icons/IconLogoGB.vue'
import LogoFooterIcon from '@/components/icons/IconLogoFooter.vue'
import { RouterLink } from 'vue-router'
</script>
<template>
  <footer class="grille space-y-6 bg-gray-900 py-16 px-6 text-white lg:space-y-0">
    <LogoFooterIcon />
    <nav class="space-y-3 lg:col-span-3 lg:col-start-7">
      <h4 class="font-bold uppercase">Menu</h4>
      <ul>
        <li><RouterLink to="/events">Agenda</RouterLink></li>
        <li><RouterLink to="/contact">Contact et accès</RouterLink></li>
      </ul>
    </nav>

    <div class="space-y-3 lg:col-span-3 lg:col-start-10">
      <h4 class="font-bold uppercase">Contact</h4>
      <address>
        1 rue Paul Koepfler<br />90000 Belfort<br />
        <a href="tel:0384542727">03 84 54 27 27</a><br />
        <a href="mailto:conservatoire@agglo-belfort.fr">conservatoire@agglo-belfort.fr</a>
      </address>
    </div>

    <div class="lg:col-span-3 lg:col-start-7"><LogoGBIcon /></div>

    <div class="space-y-3 lg:col-span-3 lg:col-start-10">
      <h4 class="font-bold uppercase">Nous suivre</h4>
      <ul class="flex gap-4">
        <li>
          <a href="https://facebook.com" aria-label="facebook"><FacebookIcon /></a>
        </li>
        <li>
          <a href="https://instagram.com" aria-label="instagram"><InstagramIcon /></a>
        </li>
        <li>
          <a href="https://twitter.com" aria-label="twitter"><TwitterIcon /></a>
        </li>
        <li>
          <a href="https://youtube.com" aria-label="youtube"><YoutubeIcon /></a>
        </li>
      </ul>
    </div>
  </footer>
</template>