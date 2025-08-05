<svg class="w-0 h-0 absolute">
  <defs>
    <clipPath id="cover-clip" clipPathUnits="objectBoundingBox">
      <polygon points="
        0.5 0,
        1 0,
        1 0.9,
        0.87 0.95,
        0.7 0.99,
        0.52 1,
        0.33 0.99,
        0.15 0.95,
        0 0.9,
        0 0
      " />
    </clipPath>
  </defs>
</svg>

<div class="relative min-h-screen bg-[#042F2E] flex flex-col max-w-2xl mx-auto">
  <div class="absolute top-0 left-0 w-full" style="z-index:1;">
    <img
      src="/coveremerald.jpg"
      alt="Wedding Couple"
      class="object-cover w-full max-h-[410px] sm:max-h-[800px] sm:max-w-[100%]"
      style="clip-path: url(#cover-clip); object-position: top;"
      draggable="false"
    />
  </div>

  <!-- Konten slice undangan di bawah gambar utama -->
  <div class="w-full flex flex-col items-center justify-center pt-8 mt-[400px] sm:mt-[800px]" style="font-family: 'Libre Caslon', serif;">
    <div class="text-[#f8f5e6] text-[11px] sm:text-lg mb-6 sm:mb-8 text-center">Dear Alan and Partner</div>
    <div class="flex flex-row items-center justify-center gap-2 mb-10 sm:mb-18">
      <span class="text-xl sm:text-4xl text-[#CA8A04] font-[GreatVibes]" style="font-family: 'Emotional Use', cursive;">Hinata</span>
      <span class="text-xl sm:text-4xl text-[#CA8A04]" style="font-family: 'Emotional Use';">&amp;</span>
      <span class="text-xl sm:text-4xl text-[#CA8A04] font-[GreatVibes]" style="font-family: 'Emotional Use', cursive;">Naruto</span>
    </div>
    <div class="text-[#f8f5e6] text-[11px] sm:text-xl mb-4 sm:mb-6 text-center">Monday, 27 July 2025</div>

    <!-- Countdown Timer Static Placeholder -->
    <div class="w-full flex flex-row items-center justify-center gap-9 sm:gap-18 mb-5">
      <div class="flex flex-col items-center">
        <span class="text-[#CA8A04] text-xl sm:text-4xl">10</span>
        <span class="text-[#f8f5e6] text-[11px] sm:text-xl mt-1">Days</span>
      </div>
      <div class="flex flex-col items-center">
        <span class="text-[#CA8A04] text-xl sm:text-4xl">20</span>
        <span class="text-[#f8f5e6] text-[11px] sm:text-xl mt-1">Hours</span>
      </div>
      <div class="flex flex-col items-center">
        <span class="text-[#CA8A04] text-xl sm:text-4xl">18</span>
        <span class="text-[#f8f5e6] text-[11px] sm:text-xl mt-1">Minutes</span>
      </div>
      <div class="flex flex-col items-center">
        <span class="text-[#CA8A04] text-xl sm:text-4xl">06</span>
        <span class="text-[#f8f5e6] text-[11px] sm:text-xl mt-1">Seconds</span>
      </div>
    </div>
  </div>

</div>
