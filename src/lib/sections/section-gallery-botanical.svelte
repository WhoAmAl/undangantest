<script lang="ts">
  import * as Carousel from "$lib/components/ui/carousel/index.js";

  import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";
    let carouselapi = $state<CarouselAPI>();
    let current = $state(0);
    $effect(() => {
    if (carouselapi) {
        current = carouselapi.selectedScrollSnap() + 1;
        carouselapi.on("select", () => {
            current = carouselapi!.selectedScrollSnap() + 1;
        });
        }
    });

    function handleCarouselAPI (api: any) {
        carouselapi = api;
        if( !carouselapi ) {
            return; 
        }
        carouselapi.on("select", () => {
            current = carouselapi!.selectedScrollSnap();
        });
        current = carouselapi.selectedScrollSnap();
    }
</script>

<div class="relative flex flex-col" style="background-image: url('/backgroundthanksbotanic.png'); background-size: cover; background-repeat: no-repeat;">
	<!-- Overlay -->
	<div class="absolute inset-0 bg-fuchsia-900/30 pointer-events-none z-10"></div>

	<!-- Main Content -->
	<div class="relative z-20 w-full flex flex-col items-center">
		<!-- Title -->
		<h2 class="mt-25 text-gray-50 text-2xl md:text-4xl font-serif drop-shadow-lg text-center tracking-wide" style="font-family: 'Oleo Script Swash Regulars', cursive;">Our Love Gallery</h2>

		<!-- Top Large Image (Video) -->
		<div class="mt-12 w-[90vw] max-w-xl aspect-[16/11] rounded-3xl overflow-hidden shadow-xl relative flex items-center justify-center bg-white/40 backdrop-blur-sm">
			<img src="/videogallerybotanical.png" alt="Gallery Main" class="w-full h-full object-cover" />
			<button class="absolute inset-0 flex items-center justify-center">
				<span class="bg-fuchsia-700 rounded-full p-4 shadow-lg">
					<svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-6.518-3.651A1 1 0 007 8.618v6.764a1 1 0 001.234.97l6.518-1.513a1 1 0 00.748-.97v-2.764a1 1 0 00-.748-.97z" /></svg>
				</span>
			</button>
		</div>

		<!-- Bottom Images -->
		<div class="mt-18 flex flex-row gap-4 justify-center items-center w-full mb-40">
			<Carousel.Root class="w-full">
                <Carousel.Content>
                    {#each Array(5) as _, i (i)}
                    <Carousel.Item class="basis-1/3 md:basis-1/3 pl-3">
                        <div class="flex h-full w-auto items-center justify-center p-0 overflow-hidden shadow">
                        <img src="/gallerypictbotanical.png" alt={`Gallery Photo ${i+1}`} class="w-full h-full object-cover" />
                        </div>
                    </Carousel.Item>
                    {/each}
                </Carousel.Content>
            </Carousel.Root>
		</div>

		  <!-- Dot Pagination -->
  <div class="flex justify-center gap-2 md:gap-3 mt-8 md:mt-2 mb-10">
      {#each Array(5) as _, index}
          <button
              class="w-2 h-2 md:w-2.5 md:h-2.5 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                  {index === current - 1
                      ? 'bg-lime-800 scale-110'
                      : 'bg-yellow-950 hover:bg-gray-800 hover:scale-105'}"
              onclick={() => carouselapi && carouselapi.scrollTo(index)}
              aria-label={`Go to story ${index + 1}`}
          ></button>
      {/each}
  </div>
	</div>
</div>