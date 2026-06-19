<template>
  <div class="bg-[#F9F9F9] min-h-screen font-sans antialiased text-gray-900 pb-16 selection:bg-[#ECA52B] selection:text-white">
    
    <main class="max-w-[480px] md:max-w-[600px] mx-auto px-4 pt-6 sm:px-6">
      
      <section class="bg-white rounded-[32px] p-6 shadow-[0_4px_24px_rgba(0,0,0,0.02)] border border-gray-100/80 mb-6">
        <h2 class="text-2xl font-black text-center text-gray-900 tracking-tight mb-6">
          Quick Rules
        </h2>
        
        <div class="grid grid-cols-3 gap-3">
          <div class="bg-gradient-to-b from-gray-50 to-white rounded-2xl p-3 border border-gray-100 flex flex-col items-center text-center shadow-sm">
            <div class="w-9 h-9 rounded-xl bg-[#ECA52B] flex justify-center items-center text-white font-black text-sm mb-3 shadow-sm shadow-[#ECA52B]/20 rotate-45">
              <span class="-rotate-45">1</span>
            </div>
            <h3 class="text-xs font-black text-gray-800 leading-tight tracking-tight">Test Beer</h3>
          </div>

          <div class="bg-gradient-to-b from-gray-50 to-white rounded-2xl p-3 border border-gray-100 flex flex-col items-center text-center shadow-sm">
            <div class="w-9 h-9 rounded-xl bg-[#ECA52B] flex justify-center items-center text-white font-black text-sm mb-3 shadow-sm shadow-[#ECA52B]/20 rotate-45">
              <span class="-rotate-45">2</span>
            </div>
            <h3 class="text-xs font-black text-gray-800 leading-tight tracking-tight">Compare styles</h3>
          </div>

          <div class="bg-gradient-to-b from-gray-50 to-white rounded-2xl p-3 border border-gray-100 flex flex-col items-center text-center shadow-sm">
            <div class="w-9 h-9 rounded-xl bg-[#ECA52B] flex justify-center items-center text-white font-black text-sm mb-3 shadow-sm shadow-[#ECA52B]/20 rotate-45">
              <span class="-rotate-45">3</span>
            </div>
            <h3 class="text-xs font-black text-gray-800 leading-tight tracking-tight">Vote</h3>
          </div>
        </div>
      </section>

      <section class="bg-white rounded-[32px] p-6 md:p-8 shadow-[0_4px_24px_rgba(0,0,0,0.02)] border border-gray-100/80 mb-8 text-center">
        <h2 class="text-2xl font-black tracking-tight text-gray-900 uppercase">
          ABOUT THE EVENT
        </h2>
        <span class="text-gray-400 font-bold text-xs uppercase tracking-widest block mt-0.5 mb-4">Seft</span>
        
        <p class="text-gray-600 leading-relaxed text-sm md:text-base mb-5 px-1">
          Welcome to the 2026 Cambodian Craft Beer Crown, the premier tasting competition celebrating local brewing passion and international excellence. Join us for an unforgettable experience featuring a premium festival atmosphere.
        </p>
        
        <span class="text-[#ECA52B] font-extrabold text-sm sm:text-base tracking-wide block border-t border-gray-50 pt-4">
          Classic European Beer Styles
        </span>
      </section>

      <section class="px-2">
        <div class="mb-4">
          <h3 class="text-2xl font-black text-gray-900 tracking-tight">Navigation Cards</h3>
          <p class="text-gray-500 text-xs mt-0.5 font-medium">Easy access for our five style.</p>
        </div>

        <div class="grid grid-cols-2 gap-4">
          <RouterLink to="/schedule" class="bg-white border border-gray-100 hover:border-[#ECA52B]/40 rounded-2xl p-5 shadow-[0_4px_16px_rgba(0,0,0,0.015)] flex flex-col items-center justify-center text-center transition-all active:scale-98 group">
            <div class="w-12 h-12 text-[#ECA52B] mb-2 flex items-center justify-center">
              <i class="fa-solid fa-calendar-days text-2xl group-hover:scale-105 transition-transform"></i>
            </div>
            <span class="font-bold text-gray-800 text-sm sm:text-base tracking-tight">Schedule</span>
          </RouterLink>

          <RouterLink to="/awards" class="bg-white border border-gray-100 hover:border-[#ECA52B]/40 rounded-2xl p-5 shadow-[0_4px_16px_rgba(0,0,0,0.015)] flex flex-col items-center justify-center text-center transition-all active:scale-98 group">
            <div class="w-12 h-12 text-[#ECA52B] mb-2 flex items-center justify-center">
              <i class="fa-solid fa-trophy text-2xl group-hover:scale-105 transition-transform"></i>
            </div>
            <span class="font-bold text-gray-800 text-sm sm:text-base tracking-tight">Awards</span>
          </RouterLink>

          <RouterLink to="/styles" class="bg-white border border-gray-100 hover:border-[#ECA52B]/40 rounded-2xl p-5 shadow-[0_4px_16px_rgba(0,0,0,0.015)] flex flex-col items-center justify-center text-center transition-all active:scale-98 group">
            <div class="w-12 h-12 text-[#ECA52B] mb-2 flex items-center justify-center">
              <i class="fa-solid fa-beer-mug-empty text-2xl group-hover:scale-105 transition-transform"></i>
            </div>
            <span class="font-bold text-gray-800 text-sm sm:text-base tracking-tight">Beer Styles</span>
          </RouterLink>

          <RouterLink to="/sponsors" class="bg-white border border-gray-100 hover:border-[#ECA52B]/40 rounded-2xl p-5 shadow-[0_4px_16px_rgba(0,0,0,0.015)] flex flex-col items-center justify-center text-center transition-all active:scale-98 group">
            <div class="w-12 h-12 text-[#ECA52B] mb-2 flex items-center justify-center">
              <i class="fa-solid fa-hand-holding-heart text-2xl group-hover:scale-105 transition-transform"></i>
            </div>
            <span class="font-bold text-gray-800 text-sm sm:text-base tracking-tight">Sponsors</span>
          </RouterLink>
        </div>
      </section>

    </main>
  </div>
</template>

<script setup>
import { RouterLink } from 'vue-router'
</script>