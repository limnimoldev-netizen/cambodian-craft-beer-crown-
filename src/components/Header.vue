<script setup>
import { RouterLink } from 'vue-router'

import { Home, Beer, Calendar, Layers, Trophy, Award } from 'lucide-vue-next'
</script>

<template>
  <header class="sticky top-0 z-50 bg-white border-b border-gray-100 shadow-sm">
    <div class="max-w-[1280px] mx-auto px-6 md:px-12">
      <div class="flex h-20 items-center justify-between">
        
        <div class="flex items-center gap-3">
          <img src="../assets/logo1.png" alt="Cambodian Beer Crown 2026" class="h-14 w-auto object-contain" />
          <img src="../assets/logo2.png" alt="Cambodian Beer Crown 2026" class="h-14 w-auto object-contain" />
        </div>

        <nav class="hidden md:flex items-center gap-8 font-medium text-base">
          <RouterLink 
            to="/home" 
            class="flex items-center gap-1.5 text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors relative"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            <i class="fa-regular fa-house"></i>
            Home
          </RouterLink>

          <RouterLink 
            to="/breweries" 
            class="flex items-center gap-1.5 text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            <Beer class="w-4 h-4" />
            Breweries
          </RouterLink>

          <RouterLink 
            to="/schedule" 
            class="flex items-center gap-1.5 text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            <Calendar class="w-4 h-4" />
            Schedule
          </RouterLink>

          <RouterLink 
            to="/styles" 
            class="flex items-center gap-1.5 text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            <Layers class="w-4 h-4" />
            Styles
          </RouterLink>

          <RouterLink 
            to="/awards" 
            class="flex items-center gap-1.5 text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            <Trophy class="w-4 h-4" />
            Awards
          </RouterLink>

          <RouterLink 
            to="/sponsors" 
            class="flex items-center gap-1.5 text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold">
            
            <i class="fa-solid fa-globe"></i>
            Sponsors
          </RouterLink>
        </nav>

        <div>
          <RouterLink 
            to="/judge" 
            class="inline-flex items-center bg-[#d48806] hover:bg-[#b57305] text-white px-6 py-2.5 rounded-full font-bold transition-all shadow-md text-base tracking-wide gap-2" >           
            <i class="fa-solid fa-check-to-slot"></i>

            Judge here
          </RouterLink>
        </div>

      </div>
    </div>
  </header>
</template>
