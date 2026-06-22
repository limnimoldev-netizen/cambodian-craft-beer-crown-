<template>
  <section class="bg-gray-50 px-4 py-16 md:py-20">
    <div class="mx-auto max-w-6xl">
      <!-- Header -->
      <div class="text-center">
        <p class="text-xs font-semibold uppercase tracking-[0.2em] text-amber-600">
          OUR SPONSORS
        </p>
        <h1 class="mt-3 text-3xl font-bold text-gray-900 sm:text-4xl">
          Sponsors at the Cambodian Craft Beer Crown 2025
        </h1>
        <p class="mx-auto mt-4 max-w-2xl text-sm text-gray-500 leading-relaxed">
          We thank our generous sponsors who make the Cambodian Craft Beer Crown 2025 possible. And  We are proud to partner with these incredible organizations who share our passion for craft beer excellence.
        </p>
        <div class="w-52 h-[3px] bg-[#EE9F27] mx-auto mt-6"></div>
      </div>

      <!-- Platinum Sponsors -->
      <div v-if="getSponsorsByTier('Platinum').length" class="mt-16">
        <div class="text-center mb-8">
          <span class="inline-block px-6 py-1.5 bg-gradient-to-r from-amber-400 to-amber-600 text-white text-xs font-semibold uppercase tracking-widest rounded-full">
            Platinum Sponsors
          </span>
        </div>
        <div 
          class="grid gap-8 max-w-4xl mx-auto justify-items-center"
          :class="getGridClass(getSponsorsByTier('Platinum').length, 'platinum')"
        >
          <div
            v-for="sponsor in getSponsorsByTier('Platinum')"
            :key="sponsor.name"
            class="group rounded-2xl border-2 border-[#C0C0C0] bg-white p-10 text-center shadow-md transition hover:shadow-xl hover:bg-gray-50 w-full max-w-sm"
          >
            <div class="mb-4 flex justify-center">
              <img 
                v-if="sponsor.logo" 
                :src="getImageUrl(sponsor.logo)" 
                :alt="sponsor.name"
                class="h-32 w-32 object-contain border-2 border-gray-200 p-3 transition group-hover:border-amber-400"
              />
              <div 
                v-else
                class="flex h-32 w-32 items-center justify-center border-2 border-gray-200 bg-amber-50 text-4xl font-bold text-amber-700 transition group-hover:border-amber-400 group-hover:bg-amber-100"
              >
                {{ getInitials(sponsor.name) }}
              </div>
            </div>
            <h3 class="text-xl font-bold text-[#EE9F27]">{{ sponsor.name }}</h3>
            <p class="mt-2 text-sm text-gray-500 leading-relaxed">
              {{ sponsor.role }}
            </p>
          </div>
        </div>
      </div>

      <!-- Gold Sponsors -->
      <div v-if="getSponsorsByTier('Gold').length" class="mt-16">
        <div class="text-center mb-8">
          <span class="inline-block px-6 py-1.5 bg-gradient-to-r from-yellow-400 to-yellow-600 text-white text-xs font-semibold uppercase tracking-widest rounded-full">
            Gold Sponsors
          </span>
        </div>
        <div 
          class="grid gap-6 max-w-5xl mx-auto justify-items-center"
          :class="getGridClass(getSponsorsByTier('Gold').length, 'gold')"
        >
          <div
            v-for="sponsor in getSponsorsByTier('Gold')"
            :key="sponsor.name"
            class="group rounded-2xl border border-[#C9A84C] bg-white p-8 text-center shadow-sm transition hover:shadow-md hover:bg-gray-50 w-full max-w-xs"
          >
            <div class="mb-4 flex justify-center">
              <img 
                v-if="sponsor.logo" 
                :src="getImageUrl(sponsor.logo)" 
                :alt="sponsor.name"
                class="h-32 w-32 object-contain border-2 border-gray-200 p-2 transition group-hover:border-amber-400"
              />
              <div 
                v-else
                class="flex h-32 w-32 items-center justify-center border-2 border-gray-200 bg-amber-50 text-4xl font-bold text-amber-700 transition group-hover:border-amber-400 group-hover:bg-amber-100"
              >
                {{ getInitials(sponsor.name) }}
              </div>
            </div>
            <h3 class="text-lg font-semibold text-[#EE9F27]">{{ sponsor.name }}</h3>
            <p class="mt-2 text-sm text-gray-500 leading-relaxed">
              {{ sponsor.role }}
            </p>
          </div>
        </div>
      </div>

      <!-- Silver Sponsors -->
      <div v-if="getSponsorsByTier('Silver').length" class="mt-16">
        <div class="text-center mb-8">
          <span class="inline-block px-6 py-1.5 bg-gradient-to-r from-gray-400 to-gray-500 text-white text-xs font-semibold uppercase tracking-widest rounded-full">
            Silver Sponsors
          </span>
        </div>
        <div 
          class="grid gap-6 max-w-5xl mx-auto justify-items-center"
          :class="getGridClass(getSponsorsByTier('Silver').length, 'silver')"
        >
          <div
            v-for="sponsor in getSponsorsByTier('Silver')"
            :key="sponsor.name"
            class="group rounded-2xl border border-[#E8E8E8] bg-white p-8 text-center shadow-sm transition hover:shadow-md hover:bg-gray-50 w-full max-w-xs"
          >
            <div class="mb-4 flex justify-center">
              <img 
                v-if="sponsor.logo" 
                :src="getImageUrl(sponsor.logo)" 
                :alt="sponsor.name"
                class="h-32 w-32 object-contain border-2 border-gray-200 p-2 transition group-hover:border-amber-400"
              />
              <div 
                v-else
                class="flex h-32 w-32 items-center justify-center border-2 border-gray-200 bg-amber-50 text-4xl font-bold text-amber-700 transition group-hover:border-amber-400 group-hover:bg-amber-100"
              >
                {{ getInitials(sponsor.name) }}
              </div>
            </div>
            <h3 class="text-base font-semibold text-[#EE9F27]">{{ sponsor.name }}</h3>
            <p class="mt-2 text-sm text-gray-500 leading-relaxed">
              {{ sponsor.role }}
            </p>
          </div>
        </div>
      </div>

      <!-- Bronze Sponsors -->
      <div v-if="getSponsorsByTier('Bronze').length" class="mt-16">
        <div class="text-center mb-8">
          <span class="inline-block px-6 py-1.5 bg-gradient-to-r from-amber-600 to-amber-800 text-white text-xs font-semibold uppercase tracking-widest rounded-full">
            Bronze Sponsors
          </span>
        </div>
        <div 
          class="grid gap-6 max-w-5xl mx-auto justify-items-center"
          :class="getGridClass(getSponsorsByTier('Bronze').length, 'bronze')"
        >
          <div
            v-for="sponsor in getSponsorsByTier('Bronze')"
            :key="sponsor.name"
            class="group rounded-2xl border border-[#CD7F32] bg-white p-6 text-center shadow-sm transition hover:shadow-md hover:bg-gray-50 w-full max-w-xs"
          >
            <div class="mb-4 flex justify-center">
              <img 
                v-if="sponsor.logo" 
                :src="getImageUrl(sponsor.logo)" 
                :alt="sponsor.name"
                class="h-32 w-32 object-contain border-2 border-gray-200 p-2 transition group-hover:border-amber-400"
              />
              <div 
                v-else
                class="flex h-32 w-32 items-center justify-center border-2 border-gray-200 bg-amber-50 text-4xl font-bold text-amber-700 transition group-hover:border-amber-400 group-hover:bg-amber-100"
              >
                {{ getInitials(sponsor.name) }}
              </div>
            </div>
            <h3 class="text-sm font-semibold text-[#EE9F27]">{{ sponsor.name }}</h3>
            <p class="mt-1 text-xs text-gray-500 leading-relaxed">
              {{ sponsor.role }}
            </p>
          </div>
        </div>
      </div>

      <!-- Partners -->
      <div v-if="getSponsorsByTier('Partner').length" class="mt-16">
        <div class="text-center mb-8">
          <span class="inline-block px-6 py-1.5 bg-gradient-to-r from-gray-300 to-gray-400 text-gray-700 text-xs font-semibold uppercase tracking-widest rounded-full">
            Partners
          </span>
        </div>
        <div 
          class="grid gap-4 max-w-5xl mx-auto justify-items-center"
          :class="getGridClass(getSponsorsByTier('Partner').length, 'partner')"
        >
          <div
            v-for="sponsor in getSponsorsByTier('Partner')"
            :key="sponsor.name"
            class="group rounded-xl border border-gray-200 bg-white p-6 text-center shadow-sm transition hover:shadow-md hover:bg-gray-50 w-full max-w-xs"
          >
            <div class="mb-3 flex justify-center">
              <img 
                v-if="sponsor.logo" 
                :src="getImageUrl(sponsor.logo)" 
                :alt="sponsor.name"
                class="h-32 w-32 object-contain border border-gray-200 p-1.5 transition group-hover:border-amber-400"
              />
              <div 
                v-else
                class="flex h-32 w-32 items-center justify-center border border-gray-200 bg-amber-50 text-4xl font-bold text-amber-700 transition group-hover:border-amber-400 group-hover:bg-amber-100"
              >
                {{ getInitials(sponsor.name) }}
              </div>
            </div>
            <h3 class="text-sm font-semibold text-[#EE9F27]">{{ sponsor.name }}</h3>
            <p class="mt-1 text-xs text-gray-500 leading-relaxed">
              {{ sponsor.role }}
            </p>
          </div>
        </div>
      </div>

      <!-- Bottom Decoration -->
      <div class="mt-16 flex items-center justify-center gap-4 text-xs text-gray-400">
        <span class="h-px w-12 bg-gray-300"></span>
        <span class="tracking-wide">Supporting Craft Beer in Cambodia</span>
        <span class="h-px w-12 bg-gray-300"></span>
      </div>
    </div>
  </section>
</template>

<script setup>
// For Vite projects
const getImageUrl = (path) => {
  if (path.startsWith('/src/') || path.startsWith('/assets/')) {
    return path
  }
  return new URL(`/src/assets/${path}`, import.meta.url).href
}

const sponsors = [
  // Platinum Sponsors (2 sponsors)
  {
    name: 'BERTIE',
    logo: 'BertiePNHlogo-3.webp',
    role: 'Official event partner.',
    tier: 'Platinum'
  },
  {
    name: 'BOTANICO',
    logo: 'botanico-spnsor.webp',
    role: 'Brewing Company',
    tier: 'Platinum'
  },
  // Gold Sponsors (3 sponsors)
  {
    name: 'CRAFT BEER ASSOCIATION',
    logo: 'CBACLOGOfa-color.webp',
    role: 'Craft Beer Association',
    tier: 'Gold'
  },
  {
    name: 'YAKIMA CHIEF',
    logo: 'CopyofLogoYakimaChiefHops.webp',
    role: 'Craft beer enthusiast group.',
    tier: 'Gold'
  },
  {
    name: 'THAI TAN',
    logo: 'CopyofLogoThaiTaneng1.webp',
    role: 'Community supporter.',
    tier: 'Gold'
  },
  // Silver Sponsors (2 sponsors)
  {
    name: 'SKAI TECH',
    logo: 'SKAI_Tech.webp',
    role: 'Event logistics partner.',
    tier: 'Silver'
  },
  {
    name: 'Bash Brewing',
    logo: 'Bash Brewing.png',
    role: 'Craft beer distributor.',
    tier: 'Silver'
  },
  // Bronze Sponsors (3 sponsors)
  {
    name: 'Black Bamboo',
    logo: 'Blackbamboo.webp',
    role: 'Event venue partner.',
    tier: 'Bronze'
  },
  {
    name: 'Projekt Brew Co.',
    logo: 'projectbrews.webp',
    role: 'Brewery partner.',
    tier: 'Bronze'
  },
  {
    name: 'Riel Brewing',
    logo: 'rielbrewing.webp',
    role: 'Distilling partner.',
    tier: 'Bronze'
  },
  // Partners (8 sponsors)
  {
    name: 'Sak Pub',
    logo: 'sakpub.webp',
    role: 'Pub partner.',
    tier: 'Partner'
  },
  {
    name: 'Brew Khnear',
    logo: 'brewkhnear.webp',
    role: 'Craft beer supplier.',
    tier: 'Partner'
  },
  {
    name: 'Chug Lab',
    logo: 'chuglab.webp',
    role: 'Brewing equipment provider.',
    tier: 'Partner'
  },
  {
    name: 'Funghi Art',
    logo: 'funghiart.webp',
    role: 'Event design partner.',
    tier: 'Partner'
  },
  {
    name: 'Fuzzy Logic',
    logo: 'fuzzylogic.webp',
    role: 'Craft beer consultant.',
    tier: 'Partner'
  },
  {
    name: 'Himawari Microbrewery',
    logo: 'Himawari Microbrewery.png',
    role: 'Microbrewery partner.',
    tier: 'Partner'
  },
  {
    name: 'Jayavara',
    logo: 'jayavara.webp',
    role: 'Hospitality partner.',
    tier: 'Partner'
  },
  {
    name: 'Krama Craft',
    logo: 'kramacraft.webp',
    role: 'Craft beer merchandise.',
    tier: 'Partner'
  }
]

// Helper function to get sponsors by tier
const getSponsorsByTier = (tier) => {
  return sponsors.filter(sponsor => sponsor.tier === tier)
}

// Helper function to get grid class based on number of items
const getGridClass = (count, tier) => {
  // For mobile: always 1 column
  // For different tiers, adjust columns based on count
  if (tier === 'platinum') {
    if (count <= 2) return 'grid-cols-1 md:grid-cols-2'
    if (count <= 3) return 'grid-cols-1 md:grid-cols-2 lg:grid-cols-3'
    return 'grid-cols-1 md:grid-cols-2 lg:grid-cols-3'
  }
  
  if (tier === 'gold' || tier === 'silver' || tier === 'bronze') {
    if (count <= 2) return 'grid-cols-1 md:grid-cols-2'
    if (count <= 3) return 'grid-cols-1 md:grid-cols-2 lg:grid-cols-3'
    if (count <= 4) return 'grid-cols-1 sm:grid-cols-2 lg:grid-cols-4'
    return 'grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4'
  }
  
  if (tier === 'partner') {
    if (count <= 2) return 'grid-cols-1 sm:grid-cols-2'
    if (count <= 3) return 'grid-cols-1 sm:grid-cols-2 lg:grid-cols-3'
    if (count <= 4) return 'grid-cols-2 sm:grid-cols-3 lg:grid-cols-4'
    if (count <= 6) return 'grid-cols-2 sm:grid-cols-3 lg:grid-cols-4'
    return 'grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5'
  }
  
  return 'grid-cols-1 sm:grid-cols-2 lg:grid-cols-3'
}

// Helper function to get initials (for fallback)
const getInitials = (name) => {
  return name
    .split(' ')
    .map(word => word.charAt(0))
    .join('')
    .substring(0, 2)
}
</script>

<style scoped>
.group {
  transition: all 0.2s ease;
}

.group:hover {
  transform: translateY(-3px);
}
</style>