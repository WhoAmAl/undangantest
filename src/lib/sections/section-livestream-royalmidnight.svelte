<!-- section-livestream-royalmidnight.svelte -->
<div class="bg-[#172554] max-w-2xl h-screen mx-auto flex flex-col relative overflow-hidden">
  <!-- Background bunga dan SVG putih, stay still -->
  <div class="absolute inset-0 w-full h-full pointer-events-none select-none z-0">
    <img src="/bungalivestreamroyalmidnight.png" alt="" class="absolute inset-0 w-full h-full object-cover object-top" draggable="false" />
    <svg
      class="absolute left-0 top-0 w-full h-full"
      viewBox="0 0 672 1195"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
      style="pointer-events: none;"
    >
      <g filter="url(#filter0_d_1222_445)">
        <path
          d="M-8 -8H680C680 -8 515 19 425 71.5C334.845 123.243 297 169 225 254C153 339 110.75 499 90 582C69.25 665 -8 1203 -8 1203V-8Z"
          fill="#FAFAFA"
          stroke="none"
        />
      </g>
      <defs>
        <filter
          id="filter0_d_1222_445"
          x="-12"
          y="-12"
          width="696.5"
          height="1219"
          filterUnits="userSpaceOnUse"
          color-interpolation-filters="sRGB"
        >
          <feFlood flood-opacity="0" result="BackgroundImageFix" />
          <feColorMatrix
            in="SourceAlpha"
            type="matrix"
            values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
            result="hardAlpha"
          />
          <feMorphology
            radius="2"
            operator="dilate"
            in="SourceAlpha"
            result="effect1_dropShadow_1222_445"
          />
          <feOffset />
          <feGaussianBlur stdDeviation="5" />
          <feComposite in2="hardAlpha" operator="out" />
          <feColorMatrix
            type="matrix"
            values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0"
          />
          <feBlend
            mode="normal"
            in2="BackgroundImageFix"
            result="effect1_dropShadow_1222_445"
          />
          <feBlend
            mode="normal"
            in="SourceGraphic"
            in2="effect1_dropShadow_1222_445"
            result="shape"
          />
        </filter>
      </defs>
    </svg>
  </div>
     
  <!-- CONTENT SECTION -->
    <div class="relative z-20 flex flex-col w-full max-w-md mx-auto mt-70 px-6 py-8 translate-x-27  ">
        <h2 class="text-white text-right text-2xl md:text-3xl font-serif tracking-widest font-semibold mb-4">LIVE STREAM</h2>
        <p class="text-white text-right text-base md:text-lg leading-relaxed mb-8">
        This live stream is our way of extending our arms across the globe to embrace each of you virtually, allowing all of you to witness, participate in, and celebrate our joy in real-time, no matter how many miles may separate us. This live stream is our way of extending our arms across the globe to embrace each of you virtually, allowing all of you to witness, participate in, and celebrate our joy in real-time, no matter how many miles may separate us. 
        </p>
        <div class="flex flex-col md:flex-row justify-center items-center gap-8 w-full">
          <!-- Instagram -->
          <div class="flex flex-col">
            <div class="flex flex-col text-center justify-center items-center gap-1 mb-2">
              <img src="/instagram.png" alt="Instagram" class="w-7 h-7 mx-auto" />
              <span class="text-white text-center text-base md:text-lg">@hinata_hyuga</span>
            </div>
            <button class="bg-white text-[#172554] rounded-full px-4 py-1 text-sm font-medium shadow-md hover:bg-gray-100 transition">
              Join Live Streaming
            </button>
          </div>
          <!-- Zoom Info -->
          <div class="flex flex-col items-center md:items-start">
            <img src="/zoom.png" alt="Zoom" class="w-7 h-7 mb-5 mx-auto" />
            <div class="text-white text-sm md:text-base leading-tight text-center md:text-left">
              ID Meeting : 123456789<br />
              Password : hariBahagia
            </div>
          </div>
        </div>
    </div>
</div>
 