<script lang="ts">
  import * as Carousel from "$lib/components/ui/carousel/index.js";
</script>

<section class="bg-[#042F2E] min-h-screen py-10 p-5 flex flex-col items-center max-w-2xl mx-auto">
  <h2 class="text-[2.5rem] font-bold text-[#F6B21B] mb-8 font-cursive tracking-wide text-center">Our Gallery</h2>
  <div class="w-full flex justify-center mb-8 relative">
    <img
      src="/galleryvideoemerald.jpg"
      alt="Gallery Cover"
      class="w-[90vw] max-w-3xl h-[320px] object-cover rounded-lg shadow-lg border-4 border-[#07332E]"
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
    <Carousel.Root class="w-full max-w-xl mb-8">
      <Carousel.Content>
        {#each Array(5) as _, i (i)}
          <Carousel.Item class="pl-1 basis-1/3.5 md:basis-1/2 lg:basis-1/3">
            <div class="flex h-[220px] w-[150px] sm:h-[280px] sm:w-full items-center justify-center p-0 overflow-hidden shadow">
              <img src="/gallerycommonemerald.jpg" alt={`Gallery Photo ${i+1}`} class="w-full h-full object-cover rounded-b-[40px] border-2 border-[#07332E]" />
            </div>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
    </Carousel.Root>
    <Carousel.Root class="w-full max-w-xl">
      <Carousel.Content>
        {#each Array(5) as _, i (i)}
          <Carousel.Item class="pl-1 basis-1/3.5 md:basis-1/2 lg:basis-1/3">
            <div class="flex h-[220px] w-[150px] sm:h-[280px] sm:w-full items-center justify-center p-0 overflow-hidden shadow">
              <img src="/gallerycommonemerald.jpg" alt={`Gallery Photo ${i+6}`} class="w-full h-full object-cover rounded-b-[40px] border-2 border-[#07332E]" />
            </div>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
    </Carousel.Root>
  </div>
</section>
