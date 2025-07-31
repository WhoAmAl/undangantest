
<script lang="ts">
// Card import removed, not needed
  import * as Carousel from "$lib/components/ui/carousel/index.js";
</script>

<div class="bg-[#172554] max-w-2xl min-h-screen sm:min-h-screen mx-auto flex flex-col items-center relative">
  <!-- Hero Image -->
  <div class="w-full flex justify-center mt-6">
    <img src="/coverroyalmidnight.png" alt="Gallery Hero" class="w-full max-w-xl aspect-[4/3] object-cover shadow-lg" />
  </div>

  <!-- Gallery Title -->
  <div class="w-full flex flex-col items-center my-8">
    <div class="bg-white w-full py-8 flex flex-row items-center justify-center gap-4 shadow">
      <img src="/butterflyleftgalleryroyalmidnight.png" alt="Butterfly Left" class="h-25 w-25 object-contain" />
      <span class="text-[#172554] tracking-[0.2em] text-lg sm:text-3xl font-serif font-semibold">OUR LOVE GALLERY</span>
      <img src="/butterflyrightgalleryroyalmidnight.png" alt="Butterfly Right" class="h-20 w-20 object-contain" />
    </div>
  </div>

  <!-- Gallery Carousel 1 -->
  <div class="w-full justify-center flex flex-col items-center">
    <Carousel.Root class="w-full max-w-xl mb-8">
      <Carousel.Content>
        {#each Array(5) as _, i (i)}
          <Carousel.Item class="pl-1 md:basis-1/2 lg:basis-1/3">
            <div class="flex aspect-[4/5] items-center justify-center p-0 rounded-md overflow-hidden shadow w-full h-full">
              <img src="/coverroyalmidnight.png" alt={`Gallery Photo ${i+1}`} class="w-full h-full object-cover" />
            </div>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
    </Carousel.Root>

    <Carousel.Root class="w-full max-w-xl">
      <Carousel.Content>
        {#each Array(5) as _, i (i)}
          <Carousel.Item class="pl-1 md:basis-1/2 lg:basis-1/3">
            <div class="flex aspect-[4/5] items-center justify-center p-0 rounded-md overflow-hidden shadow w-full h-full">
              <img src="/coverroyalmidnight.png" alt={`Gallery Photo ${i+1}`} class="w-full h-full object-cover" />
            </div>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
    </Carousel.Root>
  </div>
</div>