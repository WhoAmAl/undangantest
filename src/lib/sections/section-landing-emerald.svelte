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
      class="object-cover w-full max-h-[450px] sm:max-h-[800px] sm:max-w-[100%]"
      style="clip-path: url(#cover-clip); object-position: top;"
      draggable="false"
    />
  </div>

  <div class="absolute left-0 bottom-0 pb-18 w-full flex flex-col items-center justify-center" style="z-index:2;">
    <div class="gap-3 sm:gap-5 px-3 py-4 sm:px-6 sm:py-8 w-full flex flex-col items-center">
      <div class="text-[#FEF3C7] text-base sm:text-3xl mb-1 sm:mb-2 text-center" style="font-family: 'Oblata', serif;">
        Please Join Us | Monday, 27 July 2025
      </div>
      <div class="flex flex-row items-center justify-center gap-1 sm:gap-2 mb-4 sm:mb-6">
        <span class="text-xl sm:text-3xl text-[#e3a32b]" style="font-family: 'Emotional Use', cursive;">Hinata</span>
        <span class="text-xl sm:text-3xl text-[#e3a32b]">&amp;</span>
        <span class="text-xl sm:text-3xl text-[#e3a32b]" style="font-family: 'Emotional Use', cursive;">Naruto</span>
      </div>
      <button class="bg-[#064E3B] text-[#FEF3C7] px-3 py-1 sm:px-4 sm:py-2 rounded-[6px] sm:rounded-lg shadow-xl hover:bg-[#20675e] transition-all text-xs sm:text-sm" style="font-family: 'Oblata', serif;" onclick={handleRedirect}>Open Invitation</button>
    </div>
  </div>

</div>
