<template>
  <div class="bg-[#F9F9F9] min-h-screen font-sans antialiased text-gray-900 selection:bg-[#F0A22A] selection:text-white">
    
    <section class="relative bg-gradient-to-br from-[#0F0602] via-[#1A0B05] to-[#0F0602] min-h-[420px] md:h-[480px] flex items-center py-12 md:py-0 border-b border-gray-800">
      <div class="absolute top-1/4 right-10 w-72 h-72 bg-[#F0A22A]/10 rounded-full blur-[120px] pointer-events-none"></div>
      <div class="absolute bottom-1/4 left-10 w-48 h-48 bg-[#F0A22A]/5 rounded-full blur-[80px] pointer-events-none"></div>

      <div class="max-w-[1200px] mx-auto w-full px-6 sm:px-10 md:px-12 relative z-20 text-white">
        <div class="max-w-2xl text-center md:text-left">
          
          <h1 class="text-4xl sm:text-5xl md:text-6xl font-black tracking-tight leading-none mb-3">
            The Crown <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#F0A22A] to-[#FFC366]">2026</span>
          </h1>

          <p class="text-[#F0A22A] uppercase font-extrabold tracking-widest text-xs sm:text-sm mb-6">
            CLASSIC EUROPEAN BEER STYLES
          </p>
          
          <p class="text-gray-300 text-sm sm:text-base font-light leading-relaxed mb-8 max-w-md mx-auto md:mx-0">
            Cambodia's premier craft beer competition. Discover artisan flavors, analyze classic historic styles, and cast your vote.
          </p>
          
          <div class="flex flex-col sm:flex-row items-center justify-center md:justify-start gap-4">
            <RouterLink 
              to="/judge" 
              class="w-full sm:w-auto inline-flex items-center justify-center bg-gradient-to-r from-[#F0A22A] to-[#E09119] hover:from-[#E09119] hover:to-[#C67D11] text-white px-8 py-3.5 rounded-full font-bold tracking-wide transition-all shadow-md shadow-[#F0A22A]/10 active:scale-98"
            >
              <i class="fa-solid fa-square-check mr-2"></i>
              Judge Here
            </RouterLink>

            <RouterLink 
              to="/breweries" 
              class="w-full sm:w-auto inline-flex items-center justify-center border border-[#F0A22A] text-[#F0A22A] hover:bg-[#F0A22A] hover:text-white px-8 py-3.5 rounded-full font-bold tracking-wide transition-all"
            >
              Explore Breweries
            </RouterLink>
          </div>
        </div>
      </div>
    </section>

    <section class="max-w-[1200px] mx-auto px-6 sm:px-10 md:px-12 py-16">
      <div class="text-center mb-12">
        <h2 class="text-3xl font-black text-gray-900 tracking-tight mb-2">
          Quick Rules
        </h2>
        <div class="w-8 h-1 bg-[#F0A22A] mx-auto rounded-full"></div>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 md:gap-8">
        <div class="bg-white rounded-2xl p-8 shadow-[0_4px_20px_rgba(0,0,0,0.02)] border border-gray-100 flex flex-col items-center justify-center text-center h-48 group hover:border-[#F0A22A]/30 transition-all duration-300">
          <div class="w-12 h-12 rounded-xl bg-[#F0A22A]/10 text-[#F0A22A] font-black text-lg flex justify-center items-center mb-4 group-hover:bg-[#F0A22A] group-hover:text-white transition-colors duration-300">
            01
          </div>
          <h3 class="text-lg font-bold text-gray-800 tracking-tight">Test Beer</h3>
        </div>

        <div class="bg-white rounded-2xl p-8 shadow-[0_4px_20px_rgba(0,0,0,0.02)] border border-gray-100 flex flex-col items-center justify-center text-center h-48 group hover:border-[#F0A22A]/30 transition-all duration-300">
          <div class="w-12 h-12 rounded-xl bg-[#F0A22A]/10 text-[#F0A22A] font-black text-lg flex justify-center items-center mb-4 group-hover:bg-[#F0A22A] group-hover:text-white transition-colors duration-300">
            02
          </div>
          <h3 class="text-lg font-bold text-gray-800 tracking-tight">Compare Styles</h3>
        </div>

        <div class="bg-white rounded-2xl p-8 shadow-[0_4px_20px_rgba(0,0,0,0.02)] border border-gray-100 flex flex-col items-center justify-center text-center h-48 group hover:border-[#F0A22A]/30 transition-all duration-300">
          <div class="w-12 h-12 rounded-xl bg-[#F0A22A]/10 text-[#F0A22A] font-black text-lg flex justify-center items-center mb-4 group-hover:bg-[#F0A22A] group-hover:text-white transition-colors duration-300">
            03
          </div>
          <h3 class="text-lg font-bold text-gray-800 tracking-tight">Vote</h3>
        </div>
      </div>
    </section>

    <section class="max-w-[1200px] mx-auto px-6 sm:px-10 md:px-12 pb-24 grid grid-cols-12 gap-8 items-stretch">
      
      <div class="col-span-12 lg:col-span-5 bg-white border border-gray-100 rounded-3xl p-8 md:p-10 shadow-[0_4px_25px_rgba(0,0,0,0.02)] flex flex-col justify-between min-h-[380px]">
        <div class="my-auto text-center lg:text-left">
          <h2 class="text-2xl font-black tracking-tight text-gray-900 uppercase">
            ABOUT THE EVENT
          </h2>
          <span class="text-gray-400 font-bold text-xs uppercase tracking-widest block mt-1 mb-6">Seft</span>
          
          <p class="text-gray-600 leading-relaxed text-sm md:text-base mb-4">
            Welcome to the 2026 Cambodian Craft Beer Crown, the premier tasting competition celebrating local brewing passion and international excellence. Join us for an unforgettable experience featuring a premium festival atmosphere.
          </p>
        </div>
        
        <div class="border-t border-gray-100 pt-6 text-center lg:text-left">
          <span class="text-[#F0A22A] font-extrabold text-base tracking-wide">
            Classic European Beer Styles
          </span>
        </div>
      </div>

      <div class="col-span-12 lg:col-span-7 flex flex-col justify-center gap-6">
        
        <div class="border-l-4 border-[#F0A22A] pl-4 mb-2">
          <h3 class="text-2xl font-black text-gray-900 tracking-tight">Navigation Cards</h3>
          <p class="text-gray-500 text-xs md:text-sm mt-0.5">Easy access for our five style.</p>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <RouterLink to="/schedule" class="bg-white border border-gray-100 hover:border-[#F0A22A]/40 rounded-2xl p-6 shadow-[0_4px_15px_rgba(0,0,0,0.01)] flex flex-col items-center justify-center text-center transition-all duration-200 hover:-translate-y-0.5 group">
            <div class="w-12 h-12 rounded-xl bg-gray-50 text-[#F0A22A] mb-3 flex items-center justify-center group-hover:scale-105 transition-transform">
              <i class="fa-solid fa-calendar-days text-2xl"></i>
            </div>
            <span class="font-bold text-gray-800 text-base">Schedule</span>
          </RouterLink>

          <RouterLink to="/awards" class="bg-white border border-gray-100 hover:border-[#F0A22A]/40 rounded-2xl p-6 shadow-[0_4px_15px_rgba(0,0,0,0.01)] flex flex-col items-center justify-center text-center transition-all duration-200 hover:-translate-y-0.5 group">
            <div class="w-12 h-12 rounded-xl bg-gray-50 text-[#F0A22A] mb-3 flex items-center justify-center group-hover:scale-105 transition-transform">
              <i class="fa-solid fa-trophy text-2xl"></i>
            </div>
            <span class="font-bold text-gray-800 text-base">Awards</span>
          </RouterLink>

          <RouterLink to="/styles" class="bg-white border border-gray-100 hover:border-[#F0A22A]/40 rounded-2xl p-6 shadow-[0_4px_15px_rgba(0,0,0,0.01)] flex flex-col items-center justify-center text-center transition-all duration-200 hover:-translate-y-0.5 group">
            <div class="w-12 h-12 rounded-xl bg-gray-50 text-[#F0A22A] mb-3 flex items-center justify-center group-hover:scale-105 transition-transform">
              <i class="fa-solid fa-beer-mug-empty text-2xl"></i>
            </div>
            <span class="font-bold text-gray-800 text-base">Beer Styles</span>
          </RouterLink>

          <RouterLink to="/sponsors" class="bg-white border border-gray-100 hover:border-[#F0A22A]/40 rounded-2xl p-6 shadow-[0_4px_15px_rgba(0,0,0,0.01)] flex flex-col items-center justify-center text-center transition-all duration-200 hover:-translate-y-0.5 group">
            <div class="w-12 h-12 rounded-xl bg-gray-50 text-[#F0A22A] mb-3 flex items-center justify-center group-hover:scale-105 transition-transform">
              <i class="fa-solid fa-hand-holding-heart text-2xl"></i>
            </div>
            <span class="font-bold text-gray-800 text-base">Sponsors</span>
          </RouterLink>
        </div>

      </div>
    </section>

  </div>
</template>