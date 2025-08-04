<div class="bg-[#FECACA] flex flex-col items-center py-0 h-auto max-w-2xl mx-auto">
  <!-- Header -->
  <div class="mt-6 w-full bg-[#6B0D2B] py-6 flex justify-center">
    <h2 class="text-white text-4xl italic font-semibold tracking-wide"  style="font-family: 'Playfair Display', serif;">
      -Our Galery-
    </h2>
  </div>

  <!-- Gallery Content -->
  <div class="w-full max-w-5xl px-4 py-10 flex flex-col items-center">
    <!-- Top: Large Video/Image -->
    <div class="w-full flex justify-center mb-3 sm:mb-4">
      <div class="relative w-full max-w-2xl aspect-video overflow-hidden shadow-lg">
        <img src="/gallery1pinkcherish.png" alt="Gallery Main" class="w-full h-full object-cover" />
        <!-- Play Button Overlay (for video) -->
        <button class="absolute inset-0 flex items-center justify-center">
          <span class="bg-white bg-opacity-80 rounded-full p-2 shadow-lg sm:p-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-[#6B0D2B] sm:h-10 sm:w-10" fill="currentColor" viewBox="0 0 24 24">
              <polygon points="9,7 9,17 16,12" />
            </svg>
          </span>
        </button>
      </div>
    </div>

    <!-- Bottom: Two Images Side by Side -->
    <div class="w-full flex flex-row gap-3 sm:gap-4 justify-center">
      <div class="flex-1 max-w-md aspect-[4/5] overflow-hidden shadow-lg">
        <img src="/gallery2pinkcherish.png" alt="Gallery 1" class="w-full h-full object-cover" />
      </div>
      <div class="flex-1 max-w-md aspect-[4/5]  overflow-hidden shadow-lg">
        <img src="/gallery3pinkcherish.png" alt="Gallery 2" class="w-full h-full object-cover" />
      </div>
    </div>
  </div>
</div>