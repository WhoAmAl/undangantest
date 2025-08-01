
<script lang="ts">
// Card import removed, not needed
  import * as Carousel from "$lib/components/ui/carousel/index.js";
</script>

<div class="bg-[#172554] max-w-2xl min-h-screen sm:min-h-screen mx-auto flex flex-col items-center relative">
  <!-- Hero Image -->
  <div class="w-full flex justify-center mt-6 px-8 sm:px-0">
    <img src="/coverroyalmidnight.png" alt="Gallery Hero" class="w-full max-w-xs sm:max-w-xl h-[160px] sm:h-[350px] object-cover shadow-lg" />
  </div>

  <!-- Gallery Title -->
  <div class="w-full flex flex-col items-center my-3 sm:my-8">
    <div class="bg-white w-full py-10 sm:py-15 flex items-center justify-center shadow relative">
      <img src="/butterflyleftgalleryroyalmidnight.png" alt="Butterfly Left" class="absolute left-5 top-1/2 -translate-y-10 h-12 w-auto sm:h-20 sm:w-20 object-contain pointer-events-none select-none" />
      <span class="text-[#172554] tracking-[0.2em] text-[14px] sm:text-3xl font-serif font-semibold z-10 px-2 bg-white">
        OUR LOVE GALLERY
      </span>
      <img src="/butterflyrightgalleryroyalmidnight.png" alt="Butterfly Right" class="absolute right-5 top-1/2 -translate-y-1/2 h-12 w-auto sm:h-20 sm:w-20 object-contain pointer-events-none select-none" />
    </div>
  </div>

  <!-- Gallery Carousel 1 -->
  <div class="w-full justify-center flex flex-col items-center">
    <Carousel.Root class="w-full max-w-xl mb-1 sm:mb-8">
      <Carousel.Content>
        {#each Array(5) as _, i (i)}
          <Carousel.Item class="pl-1 basis-1/3.5 md:basis-1/2 lg:basis-1/3">
            <div class="flex h-[140px] w-[95px] sm:h-[280px] sm:w-full items-center justify-center p-0 overflow-hidden shadow">
              <img src="/coverroyalmidnight.png" alt={`Gallery Photo ${i+1}`} class="w-full h-full object-cover" />
            </div>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
    </Carousel.Root>

    <Carousel.Root class="w-full max-w-xl">
      <Carousel.Content>
        {#each Array(5) as _, i (i)}
          <Carousel.Item class="pl-1 basis-1/3.5 md:basis-1/2 lg:basis-1/3">
            <div class="flex h-[140px] w-[95px] sm:h-[280px] sm:w-full items-center justify-center p-0 overflow-hidden shadow">
              <img src="/coverroyalmidnight.png" alt={`Gallery Photo ${i+1}`} class="w-full h-full object-cover" />
            </div>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
    </Carousel.Root>
  </div>
</div>