<script lang="ts">
  import * as Carousel from "$lib/components/ui/carousel/index.js";
</script>

<div class="mx-auto max-w-2xl h-[900px] relative flex flex-col justify-center" style="background-image: url(/landingelegantlime.png); background-size: contain; background-position: center; background-repeat: no-repeat; background-attachment: fixed;">
  <svg
    class="w-full h-auto z-20 absolute top-0 left-0"
    viewBox="0 240 672 374"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    style="pointer-events: none; display: block;"
  >
    <path
      d="M672 614H671.954C671.984 612.17 672 610.337 672 608.5C672 423.208 521.568 273 336 273C150.432 273 0 423.208 0 608.5C0 610.337 0.0164441 612.17 0.0458984 614H0V0H672V614Z"
      fill="#FAFAFA"
    />
  </svg>
  <div class="absolute w-full left-0 top-[264px] z-30 text-center">
    <h1 class="font-dancing text-5xl md:text-6xl text-gray-50" style="font-family: 'Rouge Script', serif;">Our Love Gallery</h1>
  </div>
    <!-- Container for images & videos-->
  <div class="flex flex-col items-center mt-85">
    <!-- images -->
    <div class="w-full px-4 mb-4">
    <Carousel.Root class="w-full">
      <Carousel.Content>
        {#each Array(5) as _, i (i)}
          <Carousel.Item class="pl-4 md:pl-2 basis-1/3 md:basis-1/4">
            <div class="flex h-[140px] w-[95px] sm:h-[215px] sm:w-full items-center justify-center p-0 overflow-hidden shadow">
              <img src="/gallerypictelegantlime.png" alt={`Gallery Photo ${i+1}`} class="w-full h-full object-cover" />
            </div>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
    </Carousel.Root>
    </div>
    <!-- videos -->
    <div>
         <!-- Center Large Image with Play Button -->
        <div class="relative">
            <img src="/landingelegantlime.png" alt="Center Image" class="w-86 h-50 md:w-160 md:h-70 object-cover" />
            <div class="absolute inset-0 flex items-center justify-center">
                <div class="bg-lime-900 rounded-full p-2 shadow-md flex items-center justify-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 20 20">
                    <circle cx="10" cy="10" r="9" fill="transparent" />
                    <polygon points="7,6 15,10 7,14" fill="white" fill-opacity="0.8" />
                </svg>
                </div>
            </div>
        </div>
    </div>
  </div>
</div>