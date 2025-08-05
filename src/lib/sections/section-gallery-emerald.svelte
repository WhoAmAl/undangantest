<section class="bg-[#042F2E] py-10 p-5 flex flex-col items-center max-w-2xl mx-auto">
  <h2 class="text-[28px] sm:text-[36px] text-[#CA8A04] mb-8 font-cursive tracking-wide text-center" style="font-family: 'Emotional Use', cursive;">Our Gallery</h2>
  <div class="w-full flex justify-center mb-8 relative">
    <img
      src="/galleryvideoemerald.jpg"
      alt="Gallery Cover"
      class="w-[90vw] max-w-3xl h-[200px] sm:h-[320px] object-cover shadow-lg"
    />
    <button
      class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 bg-transparent rounded-full p-4 flex items-center justify-center transition"
      aria-label="Play Video"
      style="width:64px;height:64px"
    >
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" fill="none" class="w-10 h-10">
        <circle cx="24" cy="24" r="22" fill="#F6B21B" fill-opacity="0.85" />
        <polygon points="20,16 34,24 20,32" fill="white" />
      </svg>
    </button>
  </div>
  <div class="w-full flex flex-col items-center">
    <svg width="0" height="0" style="position:absolute">
      <clipPath id="photo-clip" clipPathUnits="objectBoundingBox">
        <path d="M0,0 H1 V0.856 C0.613,1 0.394,1 0,0.856 Z" />
      </clipPath>
    </svg>
    <div class="w-full max-w-xl grid grid-cols-4 gap-2 sm:gap-6">
      {#each Array(8) as _, i (i)}
        <div class="flex h-[110px] w-full sm:h-[220px] items-center justify-center p-0 overflow-visible">
          <img src="/gallerycommonemerald.jpg" alt={`Gallery Photo Static ${i+1}`} class="w-full h-full object-cover" style="clip-path: url(#photo-clip); -webkit-clip-path: url(#photo-clip); background: none; box-shadow: none;" />
        </div>
      {/each}
    </div>
  </div>
</section>
