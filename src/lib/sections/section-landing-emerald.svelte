<script>
  function handleRedirect() {
    window.location.href = '/emerald';
  }
</script>

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
      class="object-cover w-full max-h-[370px] sm:max-h-[800px] sm:max-w-[100%]"
      style="clip-path: url(#cover-clip); object-position: top;"
      draggable="false"
    />
  </div>

  <div class="absolute left-0 w-full flex flex-col items-center justify-center" style="bottom:0; z-index:2;">
    <div class="px-3 py-4 sm:px-6 sm:py-8 rounded-t-2xl shadow-lg w-full flex flex-col items-center">
      <div class="text-[#f8f5e6] text-base sm:text-xl font-serif mb-1 sm:mb-2 text-center">
        Please Join Us | Monday, 27 July 2025
      </div>
      <div class="flex flex-row items-center justify-center gap-1 sm:gap-2 mb-4 sm:mb-6">
        <span class="font-bold text-2xl sm:text-4xl text-[#e3a32b] font-[GreatVibes]">Hinata</span>
        <span class="font-serif text-xl sm:text-3xl text-[#e3a32b]">&amp;</span>
        <span class="font-bold text-2xl sm:text-4xl text-[#e3a32b] font-[GreatVibes]">Naruto</span>
      </div>
      <button class="bg-[#17443f] text-[#f8f5e6] px-2 py-0.5 sm:px-3 sm:py-1 rounded shadow-md hover:bg-[#20675e] transition-all text-xs sm:text-sm font-serif" onclick={handleRedirect}>Open Invitation</button>
    </div>
  </div>

</div>
